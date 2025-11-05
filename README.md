# 속닥속닥 : AI 감정분석 기반 정서 케어 챗봇 서비스 
## 📝 프로젝트 소개
사용자의 감정을 분석하고, 감정에 어울리는 캐릭터가 대화 상대가 되어주는 감정 기반 챗봇 어플리케이션 백엔드 서버

## 🛠 사용 기술
- FastAPI
- MySQL 8.0
- Redis

## 📊 시스템 구조도
<img width="515" height="312" alt="Image" src="https://github.com/user-attachments/assets/4aa2d29f-b76b-4e72-b4d5-7a765e449e88" />

## 🗃 ERD 설계
<img width="525" height="275" alt="Image" src="https://github.com/user-attachments/assets/7d655e41-df1a-4136-b39c-e7044d983963" />

## 🔍 주요 기능
1. 회원 관리
   - JWT 기반 인증
   - 일반 로그인
   - OAuth2.0 소셜 로그인(Naver, Google, Kakao)
   - 회원가입

2. 챗봇 대화
   - openai를 이용하여 사용자 대화
   - redis를 이용하여 대화내용 기억 하여 자연스러운 대화 유도
     
3. 대화 기록
   - 대화 종료 후 대화 내용 요약하여 일기로 저장
   - 대화 종료 시 대표감정 추출 저장
     
4. 미션 생성
   - 대화 종료 시, 대화 내용 파악 후 미션 생성을 통해 사용자 정서 케어
   - 최근 수행하지 않은 미션 중 랜덤으로 미션을 제안하도록 함
   - 미션 수행 여부와 결과는 미션 기록에 자동 반영

## 🎯 성능 개선
- 초기 대화 응답 시간 3s -> 1s로 단축
- 대화 종료 시 데이터 처리 백그라운드 실행을 통해 2s 단축

## 📚 API 문서


## 설치
```
pip install -r requirements.txt
```
