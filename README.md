# 만국박람회 [STEP 1]
> JSON 포멧의 데이터와 매칭할 모델 타입을 구현

## 📚 목차
- [팀원소개](#-팀원-소개)
- [타임라인](#-타임라인)
- [실행화면](#-실행화면)
- [트러블 슈팅](#-트러블-슈팅)
- [참고자료](#-참고자료)

## 🧑‍💻 팀원 소개
| <img src="https://i.imgur.com/8mg0oKy.jpg" width="130" height="165"/> | <img src="https://github.com/devKobe24/BranchTest/blob/main/IMG_5424.JPG?raw=true" width="200" height="200"/> |
| :-: | :-: |
| [<img src="https://hackmd.io/_uploads/SJEQuLsEh.png" width="20"/> **Mary**](https://github.com/MaryJo-github) | [<img src="https://hackmd.io/_uploads/SJEQuLsEh.png" width="20"/> **Kobe**](https://github.com/devKobe24) |

## ⏰ 타임라인
프로젝트 진행 기간 | 23.06.27.(화) ~ 23.06.30.(수)

| 날짜 | 진행 사항 |
| -------- | -------- |
| 23.06.27.(화)     | ExpoModel 생성 및 구현<br/>ItemsModel 생성 및 구현.<br/>ExpoModel 변수를 상수로 변경.<br/>ItemsModel 코드 수정, ExpoModel 코드 수정.<br/>ExpoModel unit test 추가<br/>불필요한 테스트 코드 메서드 삭제.<br/>ItemsModel 프로퍼티명 변경.<br/>ItemsModelTests 생성 및 구현.<br/>잘못된 변수명 수정.<br/>  |
| 23.06.28.(수)     | 불필요한 Assets 파일 삭제.<br/>ItemsModel의 CodingKey 삭제.<br/>ExpoModel의 visitors 타입 변경.<br/>|
| 23.06.30.(목)     | README 작성  |

## 📺 실행화면
- 만국박람회 실행 화면 <br>
<img src= "https://github.com/devKobe24/images/blob/main/%E1%84%86%E1%85%A1%E1%86%AB%E1%84%80%E1%85%AE%E1%86%A8%E1%84%87%E1%85%A1%E1%86%A8%E1%84%85%E1%85%A1%E1%86%B7%E1%84%92%E1%85%AC1.gif?raw=true" witdh="800">

## 🔨 트러블 슈팅 
1️⃣ **유닛테스트를 만드는 과정** <br>
🔒 **문제점** <br>
실제 데이터가 넘어오지 않은 상태에서 데이터가 잘 들어오는지 확인하고 싶었습니다.
그래서 어떻게 해야할지 고민이 많았습니다.

🔑 **해결방법** <br>
유닛테스트를 만들자는 결정을 했고 유닛테스트를 테스트 케이스를 통해 실제 JSON 데이터가 잘 들어오는지 확인해봤습니다.


2️⃣ **이미 선언되어 있는 프로퍼티명** <br>
🔒 **문제점 2** <br>
CodingKey 프로토콜이 CustomStringConvertible을 채택하기 때문에 description이라는 이름의 프로퍼티명을 사용할 수 없었습니다.

🔑 **해결방법** <br>
이미 JSON 데이터가 내려주는 desc라는 프로퍼티명을 사용하기로 결정했습니다.


3️⃣ **방문객의 수** <br>
🔒 **문제점 3** <br>
방문객의 수가 음수가 될 수 없다는 점을 생각하지 못하고 코드를 작성했습니다.
그래서 방문객 수의 타입은 Int형으로 지정했습니다.

🔑 **해결방법** <br>
방문객 수는 음수가 될 수 없다는 점을 인지하고 UInt 타입으로 수정하게 되었습니다.


🤔 **고민했던 점** <br>
유닛테스트를 시행시 주석과 느낌표를 사용하는데에 많은 고민을 했습니다.
주석을 사용하면 테스트를 파악하기 더 좋을것 같은 상황이지만 반대로 보면 불필요한 주석이 될 수도 있겠다는 생각도 하게 되었습니다.
또한 느낌표를 사용하는 부분에 있어서도 강제추출을 사용했을 때 옵셔널 바인딩에 실패하여 에러가 발생한다면 그것대로 에러를 잡아낸 것이라고 생각하였지만 그와 반대로 유닛테스트에서 강제추출을 사용해서는 안되는지 궁금하기도 합니다.


## 📑 참고자료
- [JSONDecoder](https://developer.apple.com/documentation/foundation/jsondecoder)
- [Using JSON with Custom Types](https://developer.apple.com/documentation/foundation/archives_and_serialization/using_json_with_custom_types)
- [Encoding and Decoding Custom Types](https://developer.apple.com/documentation/foundation/archives_and_serialization/encoding_and_decoding_custom_types)

