# 🌳 Little Forest

**개발기간** : 2025.07.23 ~ 2025.09.08 (총 44일)  
**참여인원** : 5명  
**담당업무** : 제안, 기획, 포인트 적립 시스템 구현, 담당 파트 기능 개발 및 디자인, 발표  
**개발환경** : Tomcat 8.5, Oracle DB  
**사용도구** : Figma  
**사용기술** : Spring Boot, MyBatis, Java, JavaScript, SQL, API, HTML, CSS, JSON  

---

## 📖 개요
&nbsp;&nbsp;그린핀테크는 환경적 지속가능성을 높이는 금융기술로, 디지털 기술과 녹색금융(Green Finance), 기후·환경 데이터를 활용해 기후변화와 탄소중립에 대응하는 금융 서비스입니다.  
리틀포레스트는 개인 소비자의 교통, 에너지, 쇼핑 등의 데이터를 기록한 디지털 가계부를 기반으로 친환경 소비를 관리하고, 일상 속 소비가 탄소 배출 감축 활동으로 이어지도록 지원합니다. 또한 탄소 감축 효과를 시각화하여 사용자들이 습관적으로 탄소 절감에 참여할 수 있도록 돕는 프로젝트입니다.

---

## 💡 기획 의도(동기)
&nbsp;&nbsp;2026년부터는 대기업뿐만 아니라 금융회사들도 온실가스 배출량을 공시해야 하는 ‘금융배출량(financed emissions)’의 시대가 열립니다. 이에 따라 기업뿐 아니라 개인도 자신의 탄소배출량을 직관적으로 확인하고 줄이기 위한 전략이 필요합니다. 리틀포레스트는 이러한 변화에 대응하여 **개인의 지출 내역 기반 탄소 가계부와 포인트 보상 시스템을 제공**, 친환경 소비와 저탄소 생활 습관을 유도합니다.  

---

## 🎯 목표 및 설계
### 목표
- 소비자의 계좌·결제 내역을 기반으로 탄소 소비 분석 및 시각화  
- 친환경 소비에 따른 **그린포인트 적립** 제공  
- **나무 키우기(게이미피케이션)** 기능과 친환경 제품 구매 활용  
- 사용자들의 탄소 중립 금융 습관 형성 유도  

### 📊 ERD & 테이블 설계
ERD 이미지 첨부 (https://drive.google.com/file/d/1c2CmWteDQokKMabPMcZ7VuJjKofZd2Uz/view?usp=drive_link)

<details>
<summary>📷 ERD 이미지 더보기</summary>
  
<img width="398" height="592" alt="image" src="https://github.com/user-attachments/assets/bcb4685c-67ec-40bf-91e1-251c93e85e41" />
<img width="383" height="620" alt="화면 캡처 2025-09-18 163515" src="https://github.com/user-attachments/assets/7c7d80ee-11b2-4b6e-b78a-2f7b6e5f087a" />

</details>

#### 주요 테이블
- **사용자/인증**: user_table, attendance_table  
- **지갑/결제**: wallet_table, payment_table, merchant_table  
- **탄소/포인트**: emission_table, point_table, point_event_table  
- **나무 키우기**: growing_tree_table, grown_tree_table  
- **커뮤니티**: community_table, comment_table, likes_table  
- **고객지원**: inquery_table, answer_table  
- **채팅**: chat_room_table, chat_message_table 


---

### 🛠️ 담당 역할
#### 1. **탄소 감축**
  - 사용자의 년별 탄소 감축량과 결제 내역 시각화 (calender.js)
#### 2. **로그인/회원가입**
  - 카카오 로그인 api를 사용하여 소셜 로그인 구현
  - 일반 로그인 기능
  - 통합 회원가입 페이지 구현
#### 3. **메인페이지 기능 및 디자인**
 - 메인페이지 UI/UX 설계 및 화면 구성
#### 4. **전체 웹페이지 디자인**
 - 프로젝트 전체 UI/UX 디자인 책임

---

<details>
<summary>📷 화면 구성(클릭해서 보기) </summary>


|구분 | 화면 | 미리보기 |
|----------|----------|----------|
|공통| 메인화면 | <img width="746" alt="image" src="https://github.com/user-attachments/assets/6c95713b-f8a5-45d2-8f28-81abb075366f" /> |
|공통| 회원가입 (주소api) | <img width="736" alt="image" src="https://github.com/user-attachments/assets/a63c4f22-351f-4f1b-9cf2-77495a53f5b2" /> |
|공통| 회사소개 (deeplapi) | <img width="749" height="353" alt="image" src="https://github.com/user-attachments/assets/c69ed595-ebd2-4a51-ad87-b41359c4900c" /> <img width="748" height="355" alt="image" src="https://github.com/user-attachments/assets/f7027617-4d7f-410b-b9e1-210869e166dc" /> <img width="746" height="355" alt="image" src="https://github.com/user-attachments/assets/f7f50b56-008b-4d6f-9d11-45536bc7129a" /> |
|공통| 적립방법 | <img width="741" height="357" alt="image" src="https://github.com/user-attachments/assets/8a2a88a6-7c8c-4e01-9127-9d2c8ea8a6e0" /> |
|유저| 유저채팅 | <img width="743" height="353" alt="image" src="https://github.com/user-attachments/assets/4b0193dc-6e41-40aa-b39d-199032c6cb70" /> |
|관리자| 관리자채팅| <img width="734" alt="image" src="https://github.com/user-attachments/assets/4a3681b6-f76b-4af9-bb9b-a54391470a99" /> |
|유저| 나의 지갑| <img width="750" alt="image" src="https://github.com/user-attachments/assets/cebe28e8-1a11-47d9-a746-792e7d503d28" /> |
|유저| 포인트 페이지 (다크모드) | <img width="750" alt="image" src="https://github.com/user-attachments/assets/7655bfd8-61e4-431e-9b09-cffaaaeaefeb" /> |
|유저| 기부하기 | <img width="750" alt="image" src="https://github.com/user-attachments/assets/7304c463-6872-4e76-a511-597c1f5811a7" /> <img width="750" alt="image" src="https://github.com/user-attachments/assets/abd40aa5-6683-48eb-acd2-4a65caa3b6e2" /> |
|유저| 포인트 선물하기 | <img width="939" height="489" alt="image" src="https://github.com/user-attachments/assets/a8533b00-eadc-40da-9436-0e70ec017ba7" /> |
|유저| 포인트 보상 (광고보기) | <img width="734" height="353" alt="image" src="https://github.com/user-attachments/assets/8fb213cb-c670-4eda-8576-5500eaf88d0d" /> |
|유저| 결제내역 | <img width="750" alt="image" src="https://github.com/user-attachments/assets/ebd3e3b7-aa2b-4999-8f33-78757fc65fc8" /> |
|유저| 탄소중립포인트 조회 (codef api) | <img width="800" alt="image" src="https://github.com/user-attachments/assets/3e310db2-d359-4e80-800a-8a51e0b81a4d" /> <img width="939" height="398" alt="image" src="https://github.com/user-attachments/assets/57d90ae7-59d9-4cb0-a458-77a82b214710" /> |
|유저| 나무키우기 | <img width="727" height="353" alt="image" src="https://github.com/user-attachments/assets/28763204-a6a3-4d5b-8893-591e5d7eccac" /> <img width="729" height="352" alt="image" src="https://github.com/user-attachments/assets/aabe8c4e-0b32-43e6-8520-8741f818a189" /> |
|유저| 나무키우기 (출석보상) | <img width="711" height="354" alt="image" src="https://github.com/user-attachments/assets/1a7b7dd3-69a9-45c6-a3ee-ccc215bc1875" /> |
|유저| 나무키우기 (비료구매) |<img width="715" height="353" alt="image" src="https://github.com/user-attachments/assets/66a2d028-e088-45b3-88ba-fb50acebe37d" /> |
|유저| 나무키우기 (랜덤잡초) | <img width="719" height="350" alt="image" src="https://github.com/user-attachments/assets/413bc60e-c334-47ce-b593-d3e86586ea3b" /> |
|유저| 탄소감축량 (차트&달력) | <img width="666" height="356" alt="image" src="https://github.com/user-attachments/assets/f267278d-d173-4b7b-8a17-6c4ed5ec5a1f" /> <img width="665" height="353" alt="image" src="https://github.com/user-attachments/assets/dc93e05c-7c57-43d3-a2f1-81b395c710e8" /> |
|관리자| 회원통계 | <img width="782" height="356" alt="image" src="https://github.com/user-attachments/assets/21becd59-5e0c-4aed-b2ec-a913c9756fca" /> <img width="780" height="356" alt="image" src="https://github.com/user-attachments/assets/a2bc5a0c-9142-4e86-9fed-ce83bc06bb17" /> |

</details>

---

### 🏆 성과 및 후기 
- **카카오 로그인 api 구현 성공** → 카카오톡 로그인 구현을 성공함으로써
    - API 적용 과정에서 **OAuth 2.0 인증 구조와 보안 처리의 중요성**을 학습
- **메인페이지 및 전체 웹페이지 디자인/UI 구현**  → 직관적이고 반응형 레이아웃 설계 
  - 프론트엔드 개발 과정에서 **사용자 경험(UX)과 시각적 완성도의 중요성**을 체감
- **calender.js를 활용한 탄소 감축량 표시 기능 구현** -> 사용자별 활동 이력과 절감 효과를 직관적으로 확인 가능 
  - 구현 과정에서 **데이터 시각화와 UI/UX의 결합 중요성**을 학습

<details>
<summary> 후기 더보기 </summary>


- **카카오 로그인 API 연동과 보안 처리 경험**  
  프로젝트에서 사용자 인증 방식을 구현할 때, 단순 회원가입/로그인보다는 사용자가 편리하게 접근할 수 있는 소셜 로그인 방식을 적용하고자 했습니다.
그 과정에서 카카오 로그인 API를 선택하여 OAuth 2.0 인증 구조를 이해하고 직접 적용하였습니다. 토큰 발급 및 갱신 과정, 사용자 정보 보호를 위한 보안 처리, 세션 관리 등을 구현하면서 단순히 로그인 기능 하나를 붙이는 것이 아니라, 보안성과 편의성을 동시에 고려해야 한다는 점을 배웠습니다. 특히 API 문서를 해석하고 실제 코드에 반영하는 과정에서 많은 시행착오를 겪었지만, 결과적으로 안정적인 소셜 로그인 기능을 완성할 수 있었고, 이를 통해 서비스의 접근성을 높일 수 있었습니다.  

- **프론트엔드 개발과 UI/UX 완성도 강화**  
  이번 프로젝트에서는 메인페이지와 전체적인 웹페이지 디자인을 담당하며, 단순한 화면 구성 이상의 역할을 수행했습니다. 사용자 입장에서 직관적으로 이해할 수 있는 UI를 설계하고, 반응형 레이아웃과 시각적 효과를 적용해 웹사이트의 완성도를 높였습니다. 색상 배치, 아이콘 선택, 에니메이션션 효과 등 작은 부분까지 고민하며 디자인을 진행하다 보니, 사용자가 서비스를 얼마나 편리하게 인식하는지가 프로젝트의 성패에 큰 영향을 준다는 것을 깨달았습니다. 또한 디자인과 프론트엔드 로직을 함께 다루면서, 단순히 ‘보이는 화면’을 만드는 것이 아니라, **서비스의 가치를 전달하는 경험(UX)** 을 구현하는 것이 중요하다는 점을 배우게 되었습니다.  

- **calender.js 기반 탄소 감축량 시각화 기능 구현**  
  탄소 감축량을 단순한 숫자 데이터로 보여주는 대신, 사용자들이 직관적으로 확인할 수 있도록 calender.js를 활용하여 달력 기반 시각화 기능을 구현했습니다. 이를 통해 사용자별 활동 기록과 CO₂ 절감 효과를 날짜별로 한눈에 확인할 수 있게 되었고, 탄소 절감 습관을 형성하도록 돕는 역할을 할 수 있었습니다. 구현 과정에서는 데이터 포맷을 달력 라이브러리에 맞게 가공하는 작업과, 다양한 이벤트(hover, click 등)에 따른 UI 반응을 추가하는 과정에서 많은 시행착오가 있었습니다. 하지만 이 과정을 통해 단순한 데이터 처리 이상의 **데이터 시각화와 사용자 경험 결합**의 중요성을 체감할 수 있었고, 프론트엔드 기술을 활용한 환경 데이터 전달 방식에 대해 깊이 고민해볼 수 있었습니다.  

</details>

---

### 🎥 시연 자료
- [📺 시연 영상 보기](https://drive.google.com/file/d/1KNOvw39GN9Nq5Je-ABuRC-72UrQRXZcF/view?usp=drive_link)  
- [📑 발표 자료 (PPT)](https://docs.google.com/presentation/d/16lXHTDZbE-LNdOH8F0PCaCt6K38miHoa/edit?usp=drive_link&ouid=115939005204624444347&rtpof=true&sd=true)
- [📑 발표 자료 (pdf)](https://drive.google.com/file/d/1R2O6azIVtrfG5PVHf0HQbu1ax7nbVQV5/view?usp=drive_link)
- [📑 UML](https://drive.google.com/file/d/1nqFyjvWFnB1mlrkAlK9wcyfHImJZQSMl/view?usp=drive_link)
