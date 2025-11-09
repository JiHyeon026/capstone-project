# App name : DangQ

## 설명
1) 산책 기록 및 분석 
- 지도와 연결되어 산책 경로를 실시간으로 기록 
- 속력, 거리, 시간을 측정하여 산책 활동 세밀하게 분석 
- 산책 중 좋아하는 장소와 싫어하는 장소를 마크하여 반려견의 선호도 파악 

2) 가족 간 공유 및 소통 
- 게시판을 통해 반려견 이야기를 나누고 댓글 소통 

3) 중요 일정 관리 
 - 달력 기능을 통해 예방접종, 생일, 기념일 등 반려견의 중요한 일정 표시 

4) 산책 코스 추천
다른 유저의 산책 데이터(좋아하는 곳)를 기반으로 산책 코스 추천

5) 계정을 연동하여 공동 돌봄 가능 및 추억 공유


## Backend — `my_server/`
my_server/  
├── config/                     # 서버 환경 및 설정 관련 파일  
│   ├── database.js             # 데이터베이스 연결 설정 (MySQL)  
│   └── multerConfig.js         # 파일 업로드 설정 (multer 미들웨어)  
│  
├── dogs_profile/               # 반려견 프로필 이미지 저장소  
│  
├── node_modules/               # npm 의존성 패키지  
│  
├── profile_uploads/            # 개인 프로필 이미지 저장소  
│  
├── routes/                     # Express 라우트 정의 (API 엔드포인트)  
│   ├── auth.js                 # 로그인, 회원가입, 토큰 검증 등 인증 관련  
│   ├── calendar.js             # 일정 관리 기능  
│   ├── comments.js             # 게시물 댓글 관리 기능  
│   ├── connections.js          # 가족이나 사용자 간 연결 관리  
│   ├── dog.js                  # 반려견 정보 관리 API  
│   ├── markers.js              # 지도 마커 및 위치 정보 관리  
│   ├── navigation.js           # 경로 탐색 및 네비게이션 관련 기능  
│   ├── posts.js                # 게시물 작성, 조회, 삭제  
│   ├── relationships.js        # 사용자간의 관계 관리  
│   ├── tracking.js             # 산책 기능  
│   └── users.js                # 사용자 정보 관리  
│  
├── uploads/                    # 게시판 사진 파일 업로드 저장소  
│  
├── utils/                      # 공용 유틸리티 함수 모음  
│   └── emailService.js         # 이메일 전송 서비스 (인증 메일)  
│  
├── .env                        # 환경 변수 설정 파일  
├── app.js                      # Express 앱 설정 (미들웨어 + 라우트 등록)  
├── server.js                   # 서버 실행 진입점  
├── package.json                # 프로젝트 정보 및 의존성 관리  
└── package-lock.json           # 의존성 버전 고정  


## Frontend — `lib/` (Flutter)

lib/  
├── board/                         # 게시판 관련 화면  
│   ├── board_page.dart            # 게시판 목록 화면  
│   ├── create_post_page.dart      # 게시글 작성 화면  
│   └── post_detail_page.dart      # 게시글 상세 화면  
│  
├── calendar/                      # 일정 관리 관련  
│   └── calendar.dart              # 캘린더 UI 및 일정 기능  
│  
├── login/                         # 로그인 및 회원 관련 화면  
│   ├── find_id.dart               # 아이디 찾기 화면  
│   ├── find_password.dart         # 비밀번호 찾기 화면  
│   ├── join.dart                  # 회원가입 화면  
│   ├── login.dart                 # 로그인 화면  
│   ├── password_reset.dart        # 비밀번호 재설정 화면  
│   └── widget_login.dart          # 로그인 관련 위젯 모음  
│  
├── pages/                         # 주요 앱 페이지  
│   ├── dog_profile/               # 반려견 프로필 화면  
│   └── main/                      # 메인 페이지  
│  
├── setting_pages/                 # 설정 관련 화면  
│   ├── edit_profile_page.dart     # 사용자 프로필 수정 페이지  
│   └── settings_page.dart         # 설정 메인 페이지  
│  
├── work/                          # 산책 및 위치 기반 기능  
│   ├── check_place/               # 특정 장소 확인 관련 기능  
│   │   └── selfplaceapp.dart      # 장소 체크 앱 기능  
│   ├── navigation/                # 경로 탐색 기능  
│   │   └── route_select.dart      # 경로 선택 화면  
│   ├── work_self/                 # 산책 중 기능 (속도, 시간, 드래그 등)  
│   │   ├── draggable_widget.dart  # 드래그 가능한 UI 위젯  
│   │   ├── format_utils.dart      # 포맷 관련 유틸  
│   │   ├── speed_tracker.dart     # 속도 추적 로직  
│   │   └── timer_controller.dart  # 타이머 제어 로직  
│   ├── work.dart                  # 산책 기능 메인 파일  
│   ├── dog_list.dart              # 반려견 목록 화면  
│   ├── marker_manager.dart        # 지도 마커 관리  
│   └── walk_choose.dart           # 산책 경로 선택 화면  
│  
├── work_list/                     # 산책 목록 및 경로 관련  
│   ├── work_list.dart             # 이전 산책 목록 페이지  
│   └── work_route.dart            # 특정 산책 경로 화면  
│  
├── colors.dart                    # 앱 전역 색상 설정  
└──  main.dart                     # 앱 실행 진입점  

## DATABASE
<img width="1053" height="781" alt="image" src="https://github.com/user-attachments/assets/01578c27-ad83-457e-9432-a1ff7ba9f852" />


