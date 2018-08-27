## Notification > SMS > Overview

SMS/LMS/MMS 발송, 발송 예약 기능, 템플릿 관리, 발송 내역 조회 기능을 제공하는 문자 메세지 발송 시스템입니다.
손쉬운 연동을 위한 RESTful API를 제공합니다.

## 특징

- SMS, LMS, MMS 발송을 제공합니다.
- 대량발송을 지원합니다.
  - 엑셀 파일로 수신자 목록을 입력하고 대량으로 SMS를 발송 할 수 있습니다.
- 예약 발송
  -	원하는 시간에 문자를 발송할 수 있습니다.
- 치환 태그 제공
  -	치환 태그를 이용하여 수신자 별 개별화 된 SMS 내용을 발송 할 수 있습니다.
- 템플릿 기능 제공
  - 자주 사용하는 SMS는 템플릿으로 등록하여 사용이 가능합니다.

## 주요 기능

고객의 어플리케이션에서 사용할 수 있는 문자 메세지 발송과 조회 RESTful API를 제공합니다.
SMS 발송, 발송 내역 조회, 템플릿 관리를 할 수 있는 UI를 제공합니다.


## 참고

### 태그와 UID

#### 서비스 용어
|용어|	설명|
|---|---|
|태그(tag)|UID를 분류하는 체계. <br>UID에 여러 개의 태그를 붙여 사용자가 쉽게 UID 정보를 검색하고 사용할 수 있습니다.|
|UID|사용자를 구분하는 ID(식별자). <br>하나의 UID에는 여러 개의 연락처를 등록하여 발송에 사용할 수 있습니다. |
|연락처(contact)|연락을 하기 위해 정해둔 곳. <br>Notification에서는 Push, Email, SMS, 총 3개의 상품에서 연락처를 등록할 수 있습니다. <br>Push는 토큰, Email은 메일 주소, SMS는 문자번호를 말합니다.|

#### 태그를 사용하여 발송하기
* 수신자 정보인 문자번호 대신, 태그를 선택하여 문자를 발송할 수 있는 기능을 말합니다.

1) UID를 등록합니다.

* [UID 관리]탭에서 UID와 한 개, 또는 여러 개의 문자번호를 등록합니다.
* 자세한 내용은 [[UID 관리](./console-guide/#uid)]를 참고해주세요.

2) 태그를 등록합니다.

* [태그 관리]탭에서 태그를 등록합니다.
* 자세한 내용은 [[태그 관리](./console-guide/#_15)]를 참고해주세요.

3) 태그에 UID를 등록합니다.

* [태그 관리]탭에서 등록한 태그에 UID를 등록합니다.

4) 태그를 선택한 후 문자를 발송합니다.

* [일반 발송]탭에서 메일 주소 대신 [태그 발송]을 선택하여 태그를 등록합니다.
* 메일은 태그에 등록된 UID의 문자번호로 발송됩니다.
* 자세한 내용은 [[태그를 사용한 문자발송](./console-guide/#_8)]를 참고해주세요.

#### 다른 상품의 태그 기능과의 관계
* 만약 같은 프로젝트에서 Push 또는 SMS 상품을 사용하고 있다면, Email에서 사용하고 있는 태그와 UID 정보를 재등록 없이 함께 사용할 수 있습니다.
* 각 상품의 콘솔을 통해 같은 UID에 다른 연락처 정보를 추가할 수 있습니다.