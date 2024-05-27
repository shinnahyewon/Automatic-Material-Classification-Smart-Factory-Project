# Automatic-Material-Classification-Smart-Factory-Project
Automatic Material Classification Smart Factory Project

■ 프로젝트 개요
1) 개발 배경
 디지털화는 산업체 및 제조 공장의 운영 방식을 변화시키고 있는데 디지털 세상을 위한 비디오 보안 감시, 비디오 센서, 데이터 분석 기능을 활용하는 것으로 보다 스마트해진 환경을 구축하여 건물, 자산, 작업자를 효과적으로 보호할 수 있게 된다. 하지만 현재 스마트 팩토리 시대를 맞이하고 있는 시점에서 물류 센터의 한계점을 알고 물류 센터의 문제점을 개선하고자 이러한 프로젝트를 계획하게 되었다. 

2) 개발 목표
 스마트 팩토리 시대에 맞게 인력을 대체할 물류 센터의 변화를 시각화하는 것이 목표이다. 팀에서 진행할 프로젝트로 먼저 종류에 따라 분류하는 것이다. Entry에서 나온 물품을 머시닝 센터 작업을 통해 변환한 후 트레일러로 이동시켜 시각 센서와 역반사 센서를 이용하여 물품을 인식한 후 설정해놓은 값에 따라 분류한다. 지나간 물품들이 지날 때마다 어떠한 물품이 지나갔는지 카운트해주고 지나간 물품들은 Pivot Arm Sorter Belt를 통해 지나가는 경로를 제시간에 차단시켜 물품이 정해진 구간으로 이동할 수 있게 만들어준다. 이러한 분류 방식은 인력을 감소시키는 효과가 기대되고 이는 인건비 감소로 이어지게 되어 모든 엔지니어의 목표인 비용 절감을 야기하게 될 것이다.

■ 시스템 구성
1) 프로그램 sequence 설계

![image](https://github.com/shinnahyewon/Automatic-Material-Classification-Smart-Factory-Project/assets/161293023/596aa87d-9116-4792-9bc5-7351250b95a7)

2) 코딩

![image](https://github.com/shinnahyewon/Automatic-Material-Classification-Smart-Factory-Project/assets/161293023/a30dc2c6-971f-4ae9-b36d-99c5f02e7600)

■ 주 시스템

![image](https://github.com/shinnahyewon/Automatic-Material-Classification-Smart-Factory-Project/assets/161293023/907716f6-bf4f-400a-bc72-9e559d82a695)
<전체 공정 과정>

1) 소재 생성기
 소재 생성기에서 랜덤으로 소재가 생성되면 컨베이어 벨트 위에 소재가 놓이고, 컨베이어 벨트의 이동 방향에 따라 소재를 Bases1 at entry 센서까지 이동이 되면서 또 다른 소재가 생성이 된다. 먼저 생성된 소재가 앞서 말한 센서 위치에 소재의 도착이 인식되면 공정기계가 소재를 가져가서 가공한다. 소재가 센서에 인식된 후 컨베이어 벨트는 공정이 끝날 때까지 움직이지 않는다. 가공이 끝나면 나중에 생성되었던 소재가 컨베이어 벨트의 이동 방향에 따라 소재를 Bases1 at entry 센서까지 이동시키는 것을 반복한다.

2) 이동 컨베이어 벨트
 두 공정 과정에서 생성된 소재들을 컨베이어 벨트를 이용해 Sorting station에 이동시킨다. 앞의 컨베이어 벨트에서 온 소재들을 Vision sensor1의 위치까지 이동시킨 후 Vision sensor1에 저장된 값에 따라서 소재들을 3가지로 구분한다. 가장 왼쪽의 트레일에는 Vision sensor1에 지정된 값이 9인 Metal product Base를, 가운데 트레일에는 Vision sensor1에 지정된 값이 6인 Green product Base를, 그리고 가장 오른쪽의 트레일에는 Vision sensor1에 지정된 값이 3인 Blue product Base를 구분하여 총 3가지로 분리시킨다. Vision sensor1에 인식된 소재가 Vision sensor1에 입력된 값에 따라서 분리되는 곳으로 이동될 때까지 entry Conveyour out가 멈추고 Retroreflective Sensor 5에 분리된 소재가 인식되면 분리된 소재는 분리되는 장소로 이동하고 entry Conveyour out가 움직인다.

■ 기대 목표
- 인력을 감소시키는 효과
- 스마트해진 환경을 구축하여 건물, 자산, 작업자를 효과적으로 보호
- 모든 엔지니어의 목표인 비용 감소 기대
