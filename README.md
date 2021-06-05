# CafeRecommend (카페 추천 시스템)

<!-- TABLE OF CONTENTS -->
<h2>목차</h2>
<ol>
  <li>
    <a href="#about-the-project">About the Project</a>
  </li>
  <li>
    <a href="#demo-link">Demo Link</a>
  </li>
  <li>
    <a href="#getting-started">Getting Started</a>
    <ul>
      <li><a href="#prerequisite">Prerequisite</a></li>
      <li><a href="#execution">Execution</a></li>
    </ul>
  </li>
  <li><a href="#usage">Usage</a></li>
    <ul>
      <li><a href="#login">Login</a></li>
      <li><a href="#signup">SignUp</a></li>
      <li><a href="#map">Map</a></li>
      <li><a href="#review">Review</a></li>
      <li><a href="#recommend">Recommend</a></li>
    </ul>
  <li><a href="#contributing">Contributing</a></li>
  <li><a href="#contact">Contact</a></li>
</ol>


<!-- ABOUT THE PROJECT -->
## About The Project

[![Product Name Screen Shot][product-screenshot]](https://example.com)

카카오 지도 API를 활용하여 사용자가 원하는 카페들을 지도상에서 추천해주는 서비스 입니다.

<!-- DEMO LINK -->
## Demo Link
https://2015104153.oss2021.tk:3000


<!-- GETTING STARTED -->
## Getting Started

### Prerequisite
<a href="https://nodejs.org/ko/">Node.js
  
  
<a href="https://www.mysql.com/">MySQL
  
  
<a href="https://aws.amazon.com/ko/?nc2=h_lg">AWS
  


### Execution

1. 구글 클라우드 생성 및 프로젝트 등록 후 ClientID 발급 (https://cloud.google.com/)
2. 카카오 Developer 가입 후 애플리케이션 추가 후 Javascript API키 발급 (https://developers.kakao.com/)
3. 쿠허브 repo clone
   ```sh
   git clone http://khuhub.khu.ac.kr/2015104153/CafeRecommend
   ```
4. 디렉토리 이동 후 npm 패키지 설치
   ```sh
   npm install
   ```
5. 발급받은 ClientID를 `index.js`, `index.ejs`, Javascript API키는 `map.ejs`에 각각 넣기
   ```JS
   var CLIENT_ID = "발급받은 ClientID"   // index.js
   ```
   
   ```HTML
   <meta name="google-signin-client_id" content="발급받은 ClientID"> // index.ejs
   ```
   
   ```HTML
   <script type="text/javascript" src="//dapi.kakao.com/v2/maps/sdk.js?appkey=발급받은API키&libraries=services"></script> // map.ejs
   ```
6. MySQL connection 연결 설정 (index.js)
     ```JS
     var connection = mysql.createConnection({
      host: "IP주소 입력 (localhost 또는 AWS 서버 주소)",
      user: "계정 입력",
      password: "암호 입력",
      database: "스키마이름 입력",
     });
   ```
7. 프로그램 실행
   ```sh
   npm run start
   ```

<!-- USAGE -->
## Usage

### Login & SignUp
프로그램 실행 시 최초에 나타나는 화면입니다. 구글 로그인 버튼 클릭 시에는 구글계정으로만 로그인을 수행합니다. 계정이 등록된 경우에는
바로 Map 화면으로 이동하며 그렇지 않은 경우 회원가입화면에서 닉네임(중복 불가), 나이, 성별입력 및 선호도를 선택을 수행합니다.
### Map
프로젝트 메인 화면입니다. 지도에 줌인.줌아웃이 가능하며 초기에는 사용자의 현재 위치를 기준으로 위치로 이동합니다.
API를 통해 제공된 45개의 카페가 마커형태로 나타나며 클릭 시 상세정보를 보여줍니다. 이때 후기등록 버튼 클릭시에는 후기 등록 화면으로 이동합니다. 
### Review
후기입력화면입니다. 총 4가지를 1~5점 범위에서 입력받습니다. 4가지를 모두 입력받아야 하며 등록 완료시에는 alert메시지가 나오고 Map화면으로 돌아갑니다.
### Recommend
Map에서 화면 하단의 추천 버튼 클릭 시 나타나는 화면입니다. 추천 버튼을 클릭하면 가입 시 선택했던 선호도에 맞는 카페만을 지도에 보여줍니다.
이때 추천 결과가 없는 경우에는 추천을 수행하지 않고 모든 카페를 보여줍니다.

<!-- CONTRIBUTING -->
## Contributing

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<!-- CONTACT -->
## Contact

김대철 - kdc9619@khu.ac.kr
Github Link: [https://github.com/dckat]

최정민 - cjm2021401@khu.ac.kr
Github Link: [https://github.com/cjm2021401]



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=for-the-badge
[contributors-url]: https://github.com/othneildrew/Best-README-Template/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/othneildrew/Best-README-Template.svg?style=for-the-badge
[forks-url]: https://github.com/othneildrew/Best-README-Template/network/members
[stars-shield]: https://img.shields.io/github/stars/othneildrew/Best-README-Template.svg?style=for-the-badge
[stars-url]: https://github.com/othneildrew/Best-README-Template/stargazers
[issues-shield]: https://img.shields.io/github/issues/othneildrew/Best-README-Template.svg?style=for-the-badge
[issues-url]: https://github.com/othneildrew/Best-README-Template/issues
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[license-url]: https://github.com/othneildrew/Best-README-Template/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/othneildrew
[product-screenshot]: images/screenshot.png
