# 3. Upsource 코드리뷰

[지난 2부](http://jojoldu.tistory.com/257)에 이어 이번시간엔 Upsource로 코드리뷰 과정을 소개드리겠습니다.  

## 3-1. Github Sync 주기 설정

코드리뷰를 진행하기 전에 한가지 설정을 먼저 하고 진행하겠습니다.  
Github과 Upsource의 **Sync 주기가 기본이 5분(300초)**로 잡혀있습니다.  
그래서 실제 코드가 Upsource에 반영되기가 조금 시간이 필요한데요.  
이 주기를 **30초**로 줄이겠습니다.  
  
프로젝트 페이지의 우측 상단 나사 버튼을 클릭합니다.

![upsource37](../../images/upsource37.png)

**Edit project** 를 클릭합니다.

![upsource38](../../images/upsource38.png)

300초로 되어있는 Check interval을 30으로 변경합니다.

![upsource39](../../images/upsource39.png)

**Save changes**를 클릭하면 설정이 완료됩니다.

## 3-2. 코드리뷰 

코드리뷰를 위해 Github 계정을 하나더 필요합니다.  
(리뷰어가 필요하기 때문입니다.)  
  
### 1) 프로젝트 참가 계정 추가

Github에서 계정 하나를 더 만드셨다는 가정하에 진행하겠습니다.  
다른 Github 계정 역시 설치한 Upsource 주소로 접근해 **Github 로그인**을 진행합니다.  
(관리자만 직접 로그인을 하고, 그외 계정은 Github 로그인 하시면 됩니다.)  
  
아래와 같이 가입된 계정이 2개 이상이시면 됩니다.

![upsource40](../../images/upsource40.png)

(Upsource 도메인 뒤에 ```/hub/users```를 붙이시면 해당 페이지로 이동합니다.)  

방금 가입한 2번째 계정을 샘플 프로젝트에 참가시키겠습니다.  
Upsource 도메인 뒤에 ```/hub/projects```를 붙이시면 아래와 같이 Projects 페이지로 이동됩니다.

![upsource41](../../images/upsource41.png)

여기서 원하는 프로젝트를 클릭하시면 해당 프로젝트와 관련된 설정을 할 수 있는 페이지로 이동합니다.  
**Add user or group** 버튼을 클릭해, 2번째 계정을 프로젝트 참가자로 등록합니다.

![upsource42](../../images/upsource42.png)

아래와 같이 2명이 등록된 것이 확인이 되시면 끝난 것입니다.

![upsource43](../../images/upsource43.png)

간단한 코드를 작성해서 리뷰 신청을 진행하겠습니다.

### 2) 리뷰 신청 

테스트를 위해 프로젝트에 ```feature/add-LocalDateUtil```이란 브랜치를 생성해 간단한 테스트 코드를 작성해서 commit & push하겠습니다.

![upsource44](../../images/upsource44.png)

push후, Upsource 프로젝트 페이지로 가보시면 아래와 같이 브랜치와 커밋이 올라온 것을 확인할 수 있습니다.

![upsource45](../../images/upsource45.png)

위 브랜치를 클릭하시면 아래와 같이 브랜치 페이지로 이동합니다.  
여기서 **create branch review** 버튼을 클릭합니다.

![upsource46](../../images/upsource46.png)

해당 브랜치의 코드리뷰 페이지가 생성됩니다.  
좌측을 보시면 **Reviewers +** 버튼을 클릭하시면, 아래와 같이 리뷰어 등록 Modal이 열립니다.  

![upsource47](../../images/upsource47.png)

2번째 계정을 리뷰어로 등록합니다.

![upsource48](../../images/upsource48.png)

자 그럼 이제 리뷰어로 등록된 2번째 계정으로 Upsource 페이지에 접속해 코드리뷰를 진행하겠습니다.

### 3) 리뷰어 코멘트

리뷰어로 등록된 2번째 계정으로 Upsource 에 접속해보시면 아래와 같이 리뷰 신청이 온것을 확인할 수 있습니다.

![upsource49](../../images/upsource49.png)

리뷰 브랜치를 클릭하셔서 코드리뷰를 시작합니다.  

![upsource50](../../images/upsource50.png)

17라인의 코드가 이상하니 해당 라인에 코멘트를 달겠습니다.

![upsource51](../../images/upsource51.png)

코멘트는 기본적으로 마크다운 문법을 지원합니다.

![upsource52](../../images/upsource52.png)

코멘트가 정상적으로 등록 되었습니다.

![upsource53](../../images/upsource53.png)

### 4) 리뷰이 IDE

코드리뷰를 요청한 사용자는 본인의 코드리뷰에 코멘트가 달리는 순간!  
아래와 같이 IDE에 즉각 반응이 옵니다.

![upsource54](../../images/upsource54.png)

만약 다른 파일을 열어둔 상태에서 해당 코멘트가 달린 파일로 이동하고 싶으시다면, 코멘트 위 리뷰번호 (여기선 ```ID-CR-1```)을 클릭하셔서 **Open Local File**을 클릭하면 바로 해당 파일로 이동합니다.

![upsource55](../../images/upsource55.png)

코멘트가 달린 파일에선 좌측 라인번호에 코멘트 표시가 추가됩니다.

![upsource56](../../images/upsource56.png)

우측 화면의 리뷰 코멘트에서 바로 댓글을 추가할 수 있습니다.

![upsource57](../../images/upsource57.png)

리뷰어의 화면에선 본인이 리뷰하지 않은 파일엔 Bold가 처리됩니다.

![upsource58](../../images/upsource58.png)

요청자의 코드가 잘 수정되어 더이상 리뷰할 내용이 없다면 화면 상단의 **Accept** 버튼을 클릭해 리뷰 승인을 합니다.

![upsource59](../../images/upsource59.png)

모든 리뷰어가 **Accept**를 하면 리뷰 요청자는 해당 리뷰를 Close할 수 있습니다.  

![upsource60](../../images/upsource60.png)

마지막 Close 까지 진행하면 코드리뷰가 종료됩니다.

## 3-3. Pull Request

Pull Request를 통해 코드리뷰를 진행하는 경우가 많습니다.  Upsource에도 Pull Request(이하 PR) 기능이 있기 때문에 이를 통해 코드리뷰 진행하는 과정을 진행하겠습니다.

### 1) Pull Request 설정

현재 설정으로는 바로 PR을 진행할 수 없으며, Github에서 Pull Reqeust 이벤트도 Sync 대상에 포함되도록 설정을 추가하겠습니다.  
  
Upsource 도메인에 ```/administration```로 가셔서 
Project의 **Edit proejct** 버튼을 클릭합니다.  
아래와 같은 설정 페이지에서 **Import pull requests as branches**, **Synchronize comments and pull requests**를 체크합니다.

![upsource61](../../images/upsource61.png)

인증 토큰이 있어야 하니 **Acquire synchronization token**을 클릭하셔서 토큰값을 받으면 설정은 끝납니다.

![upsource62](../../images/upsource62.png)


### 2) PR 과정

위 과정을 통해 설정이 끝나셨으면 이제 실제 PR 과정을 진행하겠습니다.  
PR 하고자하는 브랜치를 선택하셔서 우측 상단의 **Create pull request...** 를 선택합니다.

![upsource63](../../images/upsource63.png)

이번 PR에 대해 설정하는 Modal창에 PR을 받을 브랜치 (보통은 Develop가 되는데 여기선 Master에 바로 진행합니다.)를 선택합니다.

![upsource64](../../images/upsource64.png)

PR페이지가 생성되면 review 페이지와 마찬가지로 리뷰어를 등록합니다.  
이후 과정은 코드리뷰와 동일합니다.

![upsource65](../../images/upsource65.png)

리뷰어는 해당 브랜치 커밋을 보고 코드리뷰를 진행합니다.

![upsource66](../../images/upsource66.png)

코드리뷰가 모두 Accept가 되면 PR 요청자는 PR페이지 좌측 상단의 PR 링크를 클릭합니다.

![upsource67](../../images/upsource67.png)

머지될 대상인 브랜치와 Conflict 나지 않는 것을 확인후, **Merge...** 버튼을 클릭해 PR을 마무리합니다.

![upsource68](../../images/upsource68.png)

PR이 성공적으로 진행되었음을 확인할 수 있습니다.

![upsource69](../../images/upsource69.png)

여기까지! Upsource의 기본적인 사용법을 정리했습니다.  
이젠 직접 써보시면서 익히시면 충분하실것 같습니다.  
추가 팁들은 어느정도 양이 확보되면 정리하겠습니다.  
끝까지 읽어주셔서 감사합니다^^

