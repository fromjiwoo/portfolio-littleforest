### 🌳 Little Forest (그린 핀테크)

- **개발기간** : 2025.07.23 ~ 2025.09.08 (총 44일)  
- **참여인원** : 5명  
- **담당업무** : 제안, 기획, 탄소 감축량 확인 페이지 개발, 담당 파트 기능 개발, 전체 UI/UX 디자인 책임 
- **개발환경** : Tomcat 8.5, Oracle DB  
- **사용도구** : Figma  
- **사용기술** : Spring Boot, MyBatis, Java, JavaScript, SQL, API, HTML, CSS, JSON

---

#### 📖 개요
그린핀테크는 환경적 지속가능성을 높이는 금융기술로, 디지털 기술과 녹색금융(Green Finance), 기후·환경 데이터를 활용해 기후변화와 탄소중립에 대응하는 금융 서비스입니다.  

리틀포레스트는 개인 소비자의 교통, 에너지, 쇼핑 등의 데이터를 기록한 디지털 가계부를 기반으로 **친환경 소비 관리**와 **탄소 감축 참여**를 지원합니다.  
탄소 감축 효과를 시각화하여 사용자가 습관적으로 참여할 수 있도록 돕는 프로젝트입니다.

---

#### 💡 기획 의도(동기)
2026년부터 금융회사의 온실가스 배출량 공시 의무가 시작됨에 따라, **개인의 탄소 배출량 확인과 절감 전략 필요**성이 증가했습니다.  
리틀포레스트는 **개인 지출 내역 기반 탄소 가계부 + 포인트 보상 시스템**을 제공하여, 친환경 소비와 저탄소 생활 습관을 유도합니다.

---

#### 🎯 목표 및 설계
**목표**
- 소비자의 계좌·결제 내역 기반 **탄소 소비 분석 및 시각화**  
- **친환경 소비에 따른 그린포인트 적립 제공**  
- **나무 키우기(게이미피케이션) 기능과 친환경 제품 구매** 연계  
- **사용자들의 탄소 중립 금융 습관 형성 유도**

**📊 ERD & 테이블 설계**  
[ERD 이미지 보기](https://drive.google.com/file/d/1c2CmWteDQokKMabPMcZ7VuJjKofZd2Uz/view?usp=drive_link)  

**주요 테이블**
- 사용자/인증 : `user_table`, `attendance_table`  
- 지갑/결제 : `wallet_table`, `payment_table`, `merchant_table`  
- 탄소/포인트 : `emission_table`, `point_table`, `point_event_table`  
- 나무 키우기 : `growing_tree_table`, `grown_tree_table`  
- 커뮤니티 : `community_table`, `comment_table`, `likes_table`  
- 고객지원 : `inquery_table`, `answer_table`  
- 채팅 : `chat_room_table`, `chat_message_table`  

---
