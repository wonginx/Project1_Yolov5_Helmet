**프로젝트 : Yolov5 PyTorch 를 통한 배달오토바이 및 전동킥보드 헬멧착용 유무 확인 시스템						

1.목적
  1) 코로나19 사태 이후 배달서비스 수요 증대에 따라 오토바이 관련 사고 급증 / 전동킥보드 쉐어서비스 증가로 전동킥보드 사용자 급증 
    -> 5년이내 이륜차사고률 40% 증가, 이륜차 사고로 인한 치사율은 일반 자동차에 비해 2배이상 높음
  3) 현행 상 법적인 제제로 운행시 안전헬멧 미착용 벌금 부과 시행, 각종 신호위반 및 위험한 운전자 증가 
    -> 야간시간 및 보이지 않는 곳에서 미착용 / 사고발생률 및 각종 불만 증가
    -> 현행법 상 단속으로 제어하는 부분에서 한계발생 (단순히 과태료 상향 , 단속 강화로는 제한적)
    -> 사고시 큰 후유장애나 신체에 영향을 미치는 확률 증가 / 사고가해자도 피해자가 될 수 있는 상황 발생 
    -> 국가적 손실
  3) 각 배달서비스회사 및 전동킥보드 쉐어서비스 회사 그리고 범 국가적 차원에서 자동헬멧인식 모델을 이용하여 안전을 위한 체계적이고 선제적인 관리체계 필요

2. 모델구현방법
  1) Yolo_v5 PyTorch를 이용한 실시간영상분석 모델 제작 구현
  2) Data 확보는 roboflow 를 통한 open dataset 사용
  3) 오토바이, 전통킥보드 헬멧과 유사한 공사장, 현장일용직의 안전모 사진으로 dataset 구성
  4) 프로토타입 방식으로 image size 416, yolov5s 로 프로토타입 모델 제작
  5) tensorboard 로 프로토타입 모델 성능확인 및 수정
  6) 전동킥보드 영상 확보 후 영상에 프로토타입모델 적용

3. 사용방안
  1) 전동킥보드 대쉬보드 정면부에 작은 카메라 설치, 해당 카메라로 전동킥보드 쉐어 start & end 에 헬멧착용인식 여부로 동작하게 모델링 -> 비용부분 문제발생 예상
  2) 과속카메라 및 방범 및 주정차 CCTV에 해당 모델연계하여 운행시 헬멧착용유무에 대한 정확한 통계 가능성 확보 -> 추후 관리시 용이
  3) 방범 및 주정차 CCTV는 다양한 시야각을 볼수 있음으로 해당 카메라를 우선적으로 활용하여 오토바이 헬멧착용인식여부 확인 및 벌금 부과 -> 오토바이 번호판이 뒤에만 있다는 구조적 문제해결
  4) 보험사 전동킥보드 사고시 보상하는 상품판매시작 -> 2륜차 사고시 헬멧착용여부에 따른 보상 비율조정 및 보상여부 약관에 반영 -> 국가적인 법률지원필요

4. 결론
  현대 사회에서 다양한 서비스로 편리한 삶을 살고 있지만, 그 서비스 속에서 가장 중요한 unit은 컴퓨터도, 뛰어난 기술도 아닌 사람입니다. 뛰어난 배달서비스도 지금은 결국 배달해주는 사람이 있어야만 가능하고, 쉐어서비스들도 결국 사람이 이용해야합니다. 그리고 쉐어서비스 이용자와 배달오토바이 운전자들은 멀리있는 사람이 아닙니다. 당신의 아들과 딸 일수도 있으며, 가까운 친구일 수도 있습니다. 사고발생을 다양한 규제와 방법들로 억제할 순 있지만, 완전하게 막을수는 없습니다. 그렇다면 막을 수 없는 사고에서 사람의 생명만큼은 최대한 지킬 수 있는 방법을 찾아야 하고 이를 지켜야합니다. 하지만 안전불감증으로 인해 아직도 헬멧을 착용하지 않거나, 난폭한 운전으로 큰 사고들이 아직도 자주 발생하고 있습니다. 이제는 지금까지 해왔던 단순한 단속과 과태료가 아닌 AI, Computer vision과 융합하여 더욱 체계적이고 선제적인 예방으로 국민의 안전을 지켜나가기 위한 투자가 필요한 시기입니다. 
  또한 경쟁으로 고객확보, 시장점유율에만 집중투자하는 서비스 기업들은 빠른배달에 대한 투자보다 결국 배달서비스의 핵심인 배달운전자들을 위한 안전확보에 투자해야 할 시기입니다. 


5. 관련 자료
  1) 김 총리 "오토바이 신고 일제조사…'도로 위 시한폭탄' 오명 벗어야" https://view.asiae.co.kr/article/2021090210500105987 
  2) 오토바이 사고 막는다…이륜자동차 관리, 자동차 수준으로 강화 https://www.ajunews.com/view/20210902083724537
  3) 선릉역 사거리, 오토바이 아슬아슬 주행은 오늘도 그대로였다 [르포]  https://www.mk.co.kr/news/society/view/2021/08/842282/
  4) YOLOv5 https://github.com/ultralytics/yolov5



