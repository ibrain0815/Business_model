# Convai 벤치마킹 분석 보고서

> AR Agent Lab의 경쟁 분석 및 차별화 전략 수립을 위한 Convai 분석

## 1. Convai 기업 개요

### 1.1 기본 정보

| 항목 | 내용 |
|-----|------|
| **회사명** | Convai Inc. |
| **설립** | 2022년 |
| **본사** | 미국 (샌프란시스코) |
| **직원 수** | 약 43명 |
| **누적 투자** | $5M (Seed Round) |
| **2024년 매출** | $6.5M (추정) |

### 1.2 비전 및 미션

> "Create lifelike AI characters for games and virtual worlds"
> (게임과 가상 세계를 위한 생동감 있는 AI 캐릭터 생성)

**핵심 가치 제안**:
- 게임/메타버스 NPC에 대화형 AI 기능 부여
- 실시간 음성 대화 및 자연어 처리
- Unity/Unreal Engine 네이티브 통합

---

## 2. 제품 및 기술 분석

### 2.1 핵심 제품

| 제품 | 설명 | 타겟 |
|-----|------|------|
| **Convai Plugin** | Unity/Unreal 플러그인 | 게임 개발자 |
| **Character Studio** | AI 캐릭터 생성 플랫폼 | 콘텐츠 크리에이터 |
| **Voice API** | 실시간 음성 대화 API | 기업 |
| **Avatar SDK** | 3D 아바타 통합 | XR 개발자 |

### 2.2 핵심 기술 스택

```
┌─────────────────────────────────────────────────────────┐
│                    Convai Architecture                   │
├─────────────────────────────────────────────────────────┤
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐     │
│  │ Speech-to-  │  │    LLM      │  │  Text-to-   │     │
│  │   Text      │  │  Reasoning  │  │   Speech    │     │
│  └──────┬──────┘  └──────┬──────┘  └──────┬──────┘     │
│         │                │                │             │
│  ┌──────┴────────────────┴────────────────┴──────┐     │
│  │              Character Engine                  │     │
│  │  • Memory System (단기/장기 기억)              │     │
│  │  • Perception (환경 인식)                      │     │
│  │  • Action System (행동 트리거)                 │     │
│  └───────────────────────────────────────────────┘     │
│                          │                              │
│  ┌───────────────────────┴───────────────────────┐     │
│  │           Game Engine Integration             │     │
│  │      Unity SDK  |  Unreal Plugin  |  Web      │     │
│  └───────────────────────────────────────────────┘     │
└─────────────────────────────────────────────────────────┘
```

### 2.3 주요 기능

| 기능 | 설명 | 기술 수준 |
|-----|------|----------|
| **실시간 음성 대화** | 500ms 이하 응답 지연 | 상 |
| **LLM 추론** | GPT-4급 대화 능력 | 상 |
| **캐릭터 기억** | 대화 히스토리 유지 | 중상 |
| **환경 인식** | 게임 내 상황 인지 | 중상 |
| **다국어 지원** | 65+ 언어 | 상 |
| **감정 표현** | 표정/제스처 연동 | 중 |

### 2.4 지원 플랫폼

- **게임 엔진**: Unity, Unreal Engine 4/5
- **VR/AR**: Meta Quest, Apple Vision Pro, HTC Vive
- **웹**: WebGL, Three.js
- **모바일**: iOS, Android (Unity 빌드)

### 2.5 API 아키텍처 (공식 문서 기반)

Convai API는 크게 두 가지 카테고리로 구분됩니다:

```
┌─────────────────────────────────────────────────────────┐
│                    Convai API 구조                       │
├─────────────────────────────────────────────────────────┤
│                                                         │
│  ┌─────────────────────────────────────────────────┐   │
│  │           Character Crafting APIs               │   │
│  ├─────────────────────────────────────────────────┤   │
│  │ • Character API (생성/수정/삭제/복제)           │   │
│  │ • Backstory API (성격, 관계, 동기)              │   │
│  │ • Knowledge Bank API (도메인 지식 파일)         │   │
│  │ • Narrative Design API (대화 흐름/트리거)       │   │
│  │ • Action API (제스처, 이동 등)                  │   │
│  │ • Voice List API (600+ 음성 옵션)               │   │
│  │ • Chat History API (대화 히스토리 추적)         │   │
│  │ • Core AI Setting API (모델 파라미터 조정)      │   │
│  └─────────────────────────────────────────────────┘   │
│                          │                              │
│  ┌─────────────────────────────────────────────────┐   │
│  │            Interaction APIs                      │   │
│  ├─────────────────────────────────────────────────┤   │
│  │ • Standalone Voice API (STT/TTS)                │   │
│  │ • External API (제3자 서비스 연동)              │   │
│  │ • Real-time Session API                         │   │
│  └─────────────────────────────────────────────────┘   │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

### 2.6 주요 API 엔드포인트

| API | 엔드포인트 | 메서드 | 기능 |
|-----|----------|-------|------|
| **Create Character** | `/character/create` | POST | 새 캐릭터 생성 |
| **Update Character** | `/character/update` | POST | 캐릭터 정보 수정 |
| **Get Details** | `/character/get` | POST | 캐릭터 정보 조회 |
| **Clone Character** | `/user/clone_character` | POST | 캐릭터 복제 |
| **Delete Character** | `/character/delete` | POST | 캐릭터 삭제 |
| **Voice List** | `/tts/get_available_voices` | GET | 사용 가능 음성 목록 |

### 2.7 API 인증 및 요청 형식

```python
# 인증 헤더
headers = {
    "CONVAI-API-KEY": "<your-api-key>",
    "Content-Type": "application/json"
}

# 캐릭터 생성 예시
POST https://api.convai.com/character/create
{
    "charName": "AI Assistant",
    "voiceType": "MALE",
    "backstory": "You are a helpful assistant...",
    "languageCodes": ["ko", "en"],
    "actions": ["wave", "nod", "shake_head"]
}

# 응답
{
    "charID": "char_abc123xyz"
}
```

### 2.8 음성 지원 (Voice List API)

| 제공자 | 음성 수 | 특징 |
|-------|--------|------|
| **Azure Voices** | 200+ | 다국어, 고품질 |
| **ElevenLabs** | 400+ | 감정 표현, 커스텀 |
| **GCP Voices** | 100+ | 다양한 악센트 |
| **Convai Voices** | 10+ | 특수 음성 (외계인, 마녀 등) |
| **OpenAI Voices** | 6 | Alloy, Echo, Nova 등 |

### 2.9 Web SDK 구성 요소

| 컴포넌트 | 역할 | 특징 |
|---------|------|------|
| **ConvaiClient** | 연결/상태 관리 | 핵심 클래스 |
| **ConvaiWidget** | 완성형 UI | 텍스트/음성/비디오 |
| **AudioRenderer** | 음성 재생 | 필수 컴포넌트 |
| **BlendshapeQueue** | 표정 애니메이션 | ARKit(61개), MetaHuman(251개) |

### 2.10 External API 통합

Convai 캐릭터는 외부 API와 실시간 연동 가능:

```
지원 기능:
├── 날씨 API 연동 (OpenWeatherMap)
├── 티켓 시스템 (Jira, Zendesk)
├── 일정 관리 (Google Calendar)
└── 커스텀 웹훅

제약 사항:
• 최대 실행 시간: 5초
• 개발 환경: Python 3.12
• 지원 모델: GPT-4o, Claude-3.5
```

### 2.11 API 접근 제한

| 플랜 | API 접근 | 제한 |
|-----|---------|------|
| **Free** | 제한적 | Playground만 |
| **Indie Dev** | 기본 API | 일부 기능 제한 |
| **Professional+** | 전체 API | Character Crafting API 포함 |

> **주의**: Character Crafting APIs는 Professional 플랜 이상에서만 사용 가능

---

## 3. 가격 정책 분석

### 3.1 구독 플랜

| 플랜 | 월 요금 | 주요 특징 |
|-----|--------|----------|
| **Free** | $0 | 100 크레딧/월, 학습용 |
| **Indie Dev** | $29 | 1,000 크레딧, 상업적 사용 |
| **Professional** | $99 | 5,000 크레딧, 우선 지원 |
| **Scale** | $499 | 25,000 크레딧, 전용 서버 |
| **Business** | $1,199+ | 무제한, 엔터프라이즈 기능 |

### 3.2 크레딧 시스템

```
1 크레딧 = 약 1회 AI 대화 상호작용

크레딧 소모 요인:
• 음성 입력: 1 크레딧/초
• LLM 응답: 1-3 크레딧/응답
• 음성 출력: 1 크레딧/초
• 평균 대화: 5-10 크레딧/대화
```

### 3.3 가격 경쟁력 분석

| 비교 대상 | 월 비용 | 대화 수 기준 |
|---------|--------|------------|
| **Convai Professional** | $99 | ~500 대화/월 |
| **Inworld AI Pro** | $299 | ~1,000 대화/월 |
| **Character.AI Pro** | $9.99 | 개인용 (비상업) |
| **자체 구축 (Claude API)** | $50-200 | 사용량 비례 |

---

## 4. 시장 포지셔닝

### 4.1 타겟 시장

```
           게임 특화                     범용
              │
    ┌─────────┼─────────┐
    │         │         │
    │  ★Convai│  Inworld│
    │         │   AI    │
    │         │         │
B2B ┼─────────┼─────────┼ B2C
    │         │         │
    │  Epic   │Character│
    │  Games  │   .AI   │
    │         │         │
    └─────────┼─────────┘
              │
           엔터테인먼트
```

### 4.2 주요 고객 사례

| 고객 | 산업 | 활용 사례 |
|-----|-----|---------|
| **Paradox Interactive** | 게임 | NPC 대화 시스템 |
| **LG Electronics** | 가전 | AI 어시스턴트 |
| **Ready Player Me** | 메타버스 | 아바타 AI |
| **인디 게임사 다수** | 게임 | AI NPC |

### 4.3 경쟁 우위

1. **게임 엔진 통합**: Unity/Unreal 네이티브 지원
2. **실시간 성능**: 낮은 지연 시간
3. **개발자 친화적**: SDK, 문서화, 샘플 제공
4. **B2B 포커스**: 기업 고객 대상 서비스

---

## 5. AR Agent Lab vs Convai 비교

### 5.1 포지셔닝 비교

| 항목 | Convai | AR Agent Lab |
|-----|--------|--------------|
| **타겟 시장** | B2B (게임 개발사) | B2C (일반 소비자) |
| **주요 제품** | 게임 NPC AI | AR 개인비서 |
| **플랫폼** | PC/콘솔 게임 | 모바일 AR |
| **상호작용** | 게임 캐릭터 | 개인 비서 |
| **수익모델** | API/구독 (B2B) | 구독 (B2C) |

### 5.2 기술 비교

| 기술 영역 | Convai | AR Agent Lab |
|---------|--------|--------------|
| **AI 엔진** | 자체 LLM + 외부 | Claude API |
| **음성** | 실시간 TTS/STT | 모바일 네이티브 |
| **렌더링** | Unity/Unreal | Unity AR Foundation |
| **AR 지원** | 부분적 | 핵심 기능 |
| **한국어** | 65개 언어 중 1개 | 한국어 특화 |

### 5.3 차별화 기회

```
┌─────────────────────────────────────────────────────────┐
│              AR Agent Lab 차별화 포인트                  │
├─────────────────────────────────────────────────────────┤
│                                                         │
│  1. B2C 포커스                                          │
│     • Convai: 게임 개발사 대상                          │
│     • 우리: 일반 소비자 대상 개인비서                    │
│                                                         │
│  2. AR 중심 경험                                        │
│     • Convai: 게임 내 NPC                              │
│     • 우리: 실세계 증강 비서                            │
│                                                         │
│  3. 한국 시장 특화                                      │
│     • Convai: 글로벌 (한국어는 65개 중 1개)             │
│     • 우리: 한국어/문화 최적화                          │
│                                                         │
│  4. 일상 생활 통합                                      │
│     • Convai: 엔터테인먼트 목적                         │
│     • 우리: 일정, 메모, 알림 등 실용 기능               │
│                                                         │
│  5. 접근성                                              │
│     • Convai: 개발자 도구 (기술 장벽)                   │
│     • 우리: 앱 다운로드만으로 시작                      │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

---

## 6. 벤치마킹 인사이트

### 6.1 Convai에서 배울 점

| 영역 | Convai 강점 | 적용 방안 |
|-----|------------|----------|
| **기술** | 실시간 음성 대화 | 음성 상호작용 품질 강화 |
| **UX** | 캐릭터 기억 시스템 | 개인화 기억 기능 구현 |
| **비즈니스** | 크레딧 기반 과금 | 사용량 기반 플랜 검토 |
| **생태계** | SDK/플러그인 | 향후 개발자 도구 제공 |
| **API 설계** | 모듈화된 엔드포인트 | RESTful API 구조 참고 |
| **외부 연동** | External API 통합 | 제3자 서비스 연동 기능 |

### 6.2 API 설계에서 배울 점

```
Convai API 설계 원칙 → AR Agent Lab 적용

1. 캐릭터 생명주기 관리
   Convai: Create → Update → Clone → Delete
   적용: 비서 프로필 CRUD API 설계

2. 모듈화된 API 구조
   Convai: Character / Voice / Knowledge / Action 분리
   적용: 일정 / 검색 / 번역 / 알림 API 모듈화

3. 외부 서비스 연동
   Convai: External API로 실시간 정보 접근
   적용: 날씨, 교통, 뉴스 API 연동 기능

4. 음성 다양화
   Convai: 600+ 음성 옵션
   적용: 한국어 최적화 음성 5-10개 제공

5. 히스토리 관리
   Convai: Chat History API
   적용: 대화 맥락 유지 및 개인화 학습
```

### 6.3 기술 스택 비교 및 시사점

| 영역 | Convai | AR Agent Lab | 시사점 |
|-----|--------|--------------|-------|
| **LLM** | GPT-4o, Claude-3.5 | Claude 3.5 | Claude 단일화로 비용 효율 |
| **TTS** | Azure, ElevenLabs, GCP | OpenAI TTS | 한국어 품질 우선 선택 |
| **STT** | 자체 + 외부 | Whisper | 검증된 오픈소스 활용 |
| **게임엔진** | Unity, Unreal | Unity | 동일 (AR Foundation) |
| **표정** | Blendshape (61/251) | ARKit 호환 | 향후 아바타 확장 시 참고 |

### 6.2 Convai 한계점 (우리 기회)

| Convai 한계 | AR Agent Lab 기회 |
|------------|------------------|
| B2B 전용 | B2C 시장 공략 |
| 개발자 필요 | 노코드 앱 제공 |
| 게임 중심 | 일상 생활 비서 |
| 글로벌 범용 | 한국 로컬 특화 |
| 고가 ($99+/월) | 저가 (1~2만원/월) |

### 6.3 기술 로드맵 인사이트

**Convai 기술 방향**:
- 멀티모달 AI (음성 + 시각 + 텍스트)
- 장기 기억 및 관계 구축
- 환경 인식 및 반응

**우리 적용 방안**:
```
Phase 1 (MVP): 기본 음성/텍스트 대화
Phase 2 (성장): AR 공간 인식 + 개인화
Phase 3 (확장): 장기 기억 + 관계 형성
```

---

## 7. 경쟁 전략 제안

### 7.1 직접 경쟁 회피

Convai와 직접 경쟁하지 않고 **다른 시장/세그먼트** 공략:

| Convai 영역 | AR Agent Lab 영역 |
|------------|------------------|
| 게임 NPC | AR 개인비서 |
| 개발자 도구 | 소비자 앱 |
| 글로벌 | 한국 우선 |
| PC/콘솔 | 모바일 |

### 7.2 가격 전략

```
Convai 가격대: $29-1,199/월 (B2B)
AR Agent Lab 가격대: ₩0-19,900/월 (B2C)

→ 10배 저렴한 가격으로 대중 시장 진입
→ 프리미엄 (Free) 으로 사용자 확보 후 전환
```

### 7.3 마케팅 메시지

**Convai**: "Create AI characters for your game"
**AR Agent Lab**: "당신만의 AR 비서가 일상을 도와드립니다"

차별화 키워드:
- 개인비서 (vs NPC)
- 일상생활 (vs 게임)
- 누구나 (vs 개발자)
- 한국어 (vs 글로벌)

---

## 8. 결론 및 권고사항

### 8.1 핵심 결론

1. **Convai는 직접 경쟁자가 아님**
   - 타겟 시장 (B2B vs B2C), 제품 형태 (SDK vs 앱)가 다름

2. **기술적 참고 가치 높음**
   - 실시간 대화, 캐릭터 기억, 게임 엔진 통합 기술

3. **시장 검증 역할**
   - AI 캐릭터 시장의 성장 가능성 확인 ($5M 투자, $6.5M 매출)

4. **차별화 전략 명확**
   - B2C, AR, 한국어, 일상 생활, 저가격

### 8.2 사업계획서 반영 사항

- [ ] 경쟁사 분석에 Convai 추가 (간접 경쟁자)
- [ ] 기술 로드맵에 캐릭터 기억 시스템 반영
- [ ] 가격 전략 차별화 강조
- [ ] B2C vs B2B 포지셔닝 명확화

---

## 9. AR Agent Lab API 설계 권고

### 9.1 Convai 참고한 API 구조 제안

```
┌─────────────────────────────────────────────────────────┐
│              AR Agent Lab API 구조 (제안)                │
├─────────────────────────────────────────────────────────┤
│                                                         │
│  ┌─────────────────────────────────────────────────┐   │
│  │              User APIs                           │   │
│  ├─────────────────────────────────────────────────┤   │
│  │ • /user/profile - 사용자 프로필 관리            │   │
│  │ • /user/preferences - 개인 설정                 │   │
│  │ • /user/history - 대화 히스토리                 │   │
│  └─────────────────────────────────────────────────┘   │
│                                                         │
│  ┌─────────────────────────────────────────────────┐   │
│  │              Agent APIs                          │   │
│  ├─────────────────────────────────────────────────┤   │
│  │ • /agent/chat - 대화 (텍스트)                   │   │
│  │ • /agent/voice - 음성 대화 (STT/TTS)            │   │
│  │ • /agent/context - 상황 인식                    │   │
│  │ • /agent/memory - 장기 기억 관리                │   │
│  └─────────────────────────────────────────────────┘   │
│                                                         │
│  ┌─────────────────────────────────────────────────┐   │
│  │              Feature APIs                        │   │
│  ├─────────────────────────────────────────────────┤   │
│  │ • /schedule - 일정 관리                         │   │
│  │ • /search - 정보 검색                           │   │
│  │ • /translate - 실시간 번역                      │   │
│  │ • /navigate - AR 내비게이션                     │   │
│  │ • /recommend - 맞춤 추천                        │   │
│  └─────────────────────────────────────────────────┘   │
│                                                         │
│  ┌─────────────────────────────────────────────────┐   │
│  │              External APIs (연동)                │   │
│  ├─────────────────────────────────────────────────┤   │
│  │ • 캘린더 (Google, Apple, Outlook)               │   │
│  │ • 지도 (Google Maps, 카카오맵)                  │   │
│  │ • 날씨 (기상청, OpenWeatherMap)                 │   │
│  │ • 뉴스/정보 (네이버, 구글)                      │   │
│  └─────────────────────────────────────────────────┘   │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

### 9.2 개발 우선순위

| 단계 | API | 개발 시점 |
|-----|-----|---------|
| **MVP** | /agent/chat, /agent/voice | 1-3개월 |
| **Beta** | /schedule, /search, /user/* | 3-6개월 |
| **v1.0** | /translate, /navigate | 6-9개월 |
| **v2.0** | /agent/memory, /recommend | 9-12개월 |

---

*분석일: 2025-02-25*
*업데이트: 2025-02-25 (API 문서 분석 추가)*
*출처: convai.com, docs.convai.com, Tracxn, 기업 공개 정보*

**참고 문서**:
- [Convai Core API Reference](https://docs.convai.com/api-docs/api-reference/core-api-reference)
- [Character API Documentation](https://docs.convai.com/api-docs/api-reference/core-api-reference/character-crafting-apis/character-api)
- [Voice List API](https://docs.convai.com/api-docs/api-reference/core-api-reference/character-crafting-apis/voice-list-api)
- [Convai Web SDK](https://docs.convai.com/api-docs/plugins-and-integrations/web-plugins/convai-web-sdk)

