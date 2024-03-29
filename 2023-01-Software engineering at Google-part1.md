# Part 1.  전제
## Chapter 1. Software engineering이란?
> 프로그래밍과 소프트웨어 엔지니어링의 차이는 시간, 규모, 트레이드오프 세가지이다

### 시간과 변경
- 소프트웨어의 기대수명과 업그레이드의 중요도 사이에 깊은 관계가 있다.
- 소프트웨어는 시간이 지남에 따라 두가지의 변화를 견딜 수 있어야 한다.
  - 외부 환경의 변화 : 외부 소프트웨어의 동작에 의존하지 말고 계약에 의존해야 함. (하이럼의 법칙)
  - 내부 요구사항의 변화 : 소프트웨어의 변화가 지속됨에 따라 신규 코드 추가 속도가 느려지지 않아야 한다. (규모 확장과 관계가 있음)

> 하이럼의 법칙 : API 사용자가 충분히 많다면 API 명세에 적힌 내용은 중요하지 않다. 시스템에서 눈에 보이는 모든 동작을 누군가는 이용하게 될 것이다.
> - "API의 변경에 충격을 덜 받기 위해서는 동작에 의존하지 말고, 명세에 의존해야 한다."

### 규모 확장과 비용
- 소프트웨어는 조직, 시스템, 코드베이스 규모의 확장에 따라 비용이 증가하지 않거나 덜 증가하도록 해야 한다.
- 정책, 설계, 전문가그룹 등을 활용하여 세가지 영역에서 확장 가능하도록 해야 함.
- 비욘세 규칙 : "네가 좋아했다면 CI테스트를 준비했어야지"
  - 인프라팀이 공통 모듈, 코드를 수정, 배포할 권한이 있다는 뜻.
  - "언제까지 이 모듈의 버전을 각자 올려서 배포해주세요" > 인프라팀이 직접 수정, 배포
  - 전문가 팀을 활용할 분야와 enabler 팀을 활용할 분야
- 인프라는 자주 변경할수록 변경하기가 오히려 쉬워집니다.
- Shift Left : 개발과정에서 문제를 일찍 발견할수록 비용이 적게 든다.

### 트레이드오프와 비용
- 시간과 규모 확장을 견뎌야 하는 소프트웨어는 계속해서 '결정'이 필요하다.
- 측정할 수 있거나 추정할 수 있는것은 최대한 계산할 수 있어야 한다. 정량적으로 측정하기 불가능한 것에도 합리적인 결정을 위해 관심이 필요하다.
- 모든 주요 결정에 트레이드오프를 생각하고 결정해야 하며, 사전에 생각하지 못했던 비용이 발생함을 이해해야 한다.
- 시간이 지나면 환경이 달라지며, 이에 따라 기존 결정도 다시 살펴보고 재고해야 한다.

> 생각해볼 것들
> - 기본적인 인프라 비용, 인건비 계산식을 정리하고 공유하고 업데이트 해보자.
> - 장애대응 프로세스를 숙달하기 위해 주기적으로 모의 훈련을 해보자.

----

## Chapter 2. 팀워크 이끌어내기

> 소프트웨어 개발은 '팀의 단합된 노력'의 결실이다. 그래서 엔지니어링 팀이 성공하려면 겸손, 존중, 신뢰라는 핵심원칙에 맞게 우리 자신의 행동을 바로잡아야 한다. 

### 천재 신화를 버려라.
- 리누스 토발츠의 진짜 업적은 이 사람들을 협업하게 이끈 것입니다.

### 숨기는 것은 해롭다.
- 자신이 올바른 길을 걷고 있음을 어떻게 확인할 수 있을까요?
- 조기 감지가 필요하다.
- 버스지수 : 몇 명의 팀원이 버스에 치어서 일을 할 수 없게 될 때 프로젝트가 망하게 되는지를 나타내는 지수

### 모든 것은 팀에 달렸다.
- 비전을 공유하세요, 역할을 나누세요, 다른 이로부터 배우세요, 멋진팀을 만드세요
- 사회적 상호작용의 세 기둥 : 겸손, 존중, 신뢰
- 겸손 : 당신은 모든 것을 알지도, 완벽하지도 않습니다. 겸손한 사람은 배움에 열려있습니다.
- 존중 : 동료를 진심으로 생각합니다. 친절하게 대하고 그들의 능력과 성취에 감사해야 합니다.
- 신뢰 : 동료들이 유능하고 올바른 일을 하리라 믿습니다. 필요하면 그들에게 스스로 방향을 정하게 해도 좋습니다.
- 관계는 언제나 프로젝트보다 오래 지속됩니다
- 비난없는 포스트모템 문화
- 다른 이로부터 배우는 데 열려 있을수록 여러분의 영향력도 커집니다. 결점이 많은 사람일수록 더 강해보입니다.
- 결점을 드러낸다는 것은 겸손을 겉으로 표현하는 일이며, 책임을 지고 의무를 다 하려는 의지의 표출입니다. 다른 이들의 의견을 신뢰한다는 신호이기도 합니다.

> 생각할 것들
> - 버스지수를 최소 2로, 일반적으로는 3 이상으로 하자
> - 포스트모템은 실무자 중심으로 진행하고, 관리자에게는 보고하면 어떨까?
> - 설계 커뮤니티를 만들어 보자. (설계는 Advise 방식 고려. martin fowler.com참고)

----

## Chapter 3. 지식 공유
> 핵심 메시지
> - 조직은 자신의 문제 대부분에 스스로 답할 수 있어야 한다.
> - 조직 내에 전문가들이 필요하고 그들의 지식을 전파할 메커니즘이 필요하다.
> - 조직 내에 배움의 문화가 자리잡혀야 한다.

### 배움을 가로막는 장애물
- `가면 증후군`: 자신의 능력보다 과대펴가 받고 있다고 느껴서, 자칫 실수하면 자신이 사기꾼임을 들킬지 모른다는 두려움
- 심리적 안전 부족 : 모른다는 사실을 숨기려는 경향으로 나타남
- 정보 섬 : 일하는 방식을 각각의 부서가 제각기 만들어 나감
  - 정보 파편화 : 섬마다 서로 다른 그림을 그리고 그마저도 불완전함
  - 정보 중복 : 섬마다 나름의 작업 방식을 재창조함
  - 정보 왜곡 : 같은 일이라도 섬마다 작업 방식이 다르고, 심지어 충돌함
- 단일 장애점 : '여러분을 위해 내가 다 처리하지' -> 단기 효율을 높여주는 대신 장기 확장성을 희생
- 전부 아니면 전무 전문성 (all-or-nothing expertise) : 모든 것을 아는 사람과 아무것도 모르는 초심자

### 철학
- 소프트웨어 엔지니어링에서 가장 중요한 요소는 '사람'이다
- 전문가의 일대일 조언은 효과적이지만, 확장성이 부족하여 팀이 커지면 유용하지 못함
- 문서화된 지식은 확장성이 좋지만, 개별학습자가 처한 특수한 상황에 부적합할 수 있고, 유지보수 비용이 듬
- 개개인의 지식과 문서화된 정보 중간 어딘가에 '현장지식(contextual knowledge)'이 존재
- 한 조직이 담고 있는 지식은 세월이 흐르면 변화하며 가장 적합한 지식 공유방법도 조직 규모가 커감에 따라 달라진다
- 조직 스스로 교육하고, 배우고 성장하는데 집중하고, 충분한 수의 전문가를 양성해야 한다.

### 심리적 안전감
- 사람들이 당연한 사실을 모른다고 해서 놀라지 않는다. 왜냐하면 미국에서 성인이라면 누구나 아는 상식을 생전 처음 듣는 사람의 수가 매일 평균 1만명은 되기 때문이다.
- 멘토 제도 : 온보딩 프로세스. 멘티가 더 편하게 질문할 수 있도록 멘토는 멘티와 같은 팀의 일원이어서는 안됨
- 낯선 이들로 구성된 전문가 그룹보다 바로 옆 동료가 편하다. 그룹에서 심리적 안전감이 더 필요하며, 적대적이지 않고 협조적으로 일하는 문화가 중요하다.
  - 기초적인 질문, 실수를 올바른 방향으로 안내 vs 실수를 꾸짖기
  - 질문자가 배우게끔 도와줄 목적 vs 내 지식을 뽐낼 목적
  - 상냥하게 인내심을 가지고 도움을 줌 vs 잘난 체하고 비난함
  - 해법을 찾기 위해 공개 토론 형식 vs '승자'와 '패자'를 가리는 논쟁 형식

### 내 지식 키우기
- 항상 배우고 항상 질문하라
- 초심자가 저지르는 가장 큰 실수는 무언가 막혔을 때 질문하지 않는 것이다 (너무 '기초적인'질문이란 소리를 듣기 싫어서). 모르는 분야가 나오면 두려워하지 말고 성장하는 기회로 받아들여라
- '상급자라면 모든 걸 알아야 한다'는 인식이 생기지 않도록 주의하라. 
- 많이 알면 알수록 모르는 것이 더 많음을 깨닫게 된다
- `'무언가를 옮기거나 바꾸려면 그게 왜 그자리에 있는지부터 이해하자'`

### 커뮤니티에 묻기
- 그룹채팅, 메일링 리스트, 질의응답 시스템
- 그룹채팅
  - 주제나 팀별로 개설
  - 간단한 질문에 적합
  - 본인이 적극적으로 참여하지 않은 대화에서는 의미있는 정보를 뽑아내기 어려울 수 있음
- 메일링 리스트
  - 맥락정보가 많이 필요한 복잡한 질문에 적합하지만, 빠르게 주고받는 대화에 취약
  - 이메일 아카이브는 내용을 수정할 수 없어 찾은 정보가 지금도 유효한지 확인하기 어려움
- 스택 오버플로우 같은 플랫폼

### 지식 확장하기 (가르치기)
- 가르친다는 것은 전문가의 전유물이 아니다. 전문성은 다차원 벡터이다
- 오피스아워 : 누군가가 특정 주제에 관한 질문에 답해줄 목적으로 시간을 비워 둔 정기적인 이벤트
  - 문서화되지 않은 특수한 문제에 맞닥뜨렸을 때 특히 유용
- 기술 강연 : 연사가 청중에게 직접 강의
- 수업 : 실습을 포함. 강연보다 관리 비용이 더 많이 들어서 가장 중요하거나 어려운 주제에 배정됨. 한번 개설하면 동일 교재를 재활용할 수 있어서 비교적 쉽게 규모를 늘릴 수 있다
- g2g : 동료직원을 위한 수업을 개설, 참석. 수업은 강연보다 실습을 포함하는 경우가 많음
- 문서자료 : 독자가 무언가를 배우도록 돕는 것을 최우선 목표로 하는 기록된 지식
  - 문서자료 소유자가 누구든 모든 엔지니어에게 갱신 권한이 있다
  - 문서자료 변경 이력도 코드 이력과 똑같은 방식으로 추적할 수 있다
  - 문서자료에는 피드백할 방법이 있어야 한다
  - 문서화는 소수가 시간을 들여 다수에게 이득을 주므로 조직 전체에 도움을 주지만, 기여자와 수혜자가 달라서 적절한 보상 없이는 사람들을 움직이게 하기 어렵다

### 조직의 지식 확장하기
- 코드 같은 산출물보다 문화와 환경을 첫 번째로 두고 생각해야 더 나은 결과를 얻는다고 믿는다
- `기술업계에서는 뛰어난 괴짜를 용인하는 경향이 있지만, 해로운 현상이다.` 몇몇 개인의 나쁜 행동 때문에 팀 전체가 초심자에게 버티기 가혹한 환경으로 변하게 두어서는 안된다
- 지식 공유 문화를 장려하려면 인정과 보상 제도가 뒷받침 되어야 한다 (회사의 성과검토, 승진 기준, 동료사이의 상)
- '표준 정보 소스 구축' : 회사 차원의 중앙집중적 정보 원천. 전문가의 지식을 표준화하고 전파하는 수단
  - 해당 분야 전문가들이 적극적으로 관리하고 감독해야 함
  - 복잡한 주제일수록 소유자를 명확히 정해둬야 함
- 공식 개발자 가이드 : 코딩 스타일 가이드, 소프트웨어 엔지니어링 모범사례, 코드 리뷰 가으디, 테스트 가이드, 금주의 팁
- go/ 링크 : go/python, go/spanner 등 표준 정보소스로 링크
- 코드랩 : 동작하는 예시코드, 설명, 코딩 연습문제 등을 활용해 엔지니어에게 새로운 개념, 프로세스를 가르치는 실습형 튜토리얼
- 정적 분석 : 코딩 가이드나 모범사례를 적용해 개선할 수 있는 코드를 찾아 리뷰어에게 알려줌. 개선사항을 자동으로 적용

### `가독성 제도`
- 프로그래밍 언어 모범 사례를 전파하기 위한 전사 차원으 '표준 멘토링 프로세스'
- 언어 이디엄, 코드 구조, API 설계, 공통 라이브러리의 올바른 사용법, 문서화, 테스트 커버리지 등 전문 지식을 광범위하게 다룸
- 모든 CL은 가독성 승인을 얻어야 함
  - 해당 언어의 가독성 자격증이 있는 누군가가 해당 CL을 승인
  - 본인의 CL은 암묵적으로 이뤄짐
  - 약 1~2% 구글 엔지니어가 가독성 리뷰어로 활동
  - 리뷰어는 자신의 제안을 뒷받침하는 인용을 제공하여 이론적인 근거를 배울 수 있게 함
  - 가독성 제도는 '코드 리뷰가 길어진다는 단기적인 비용'과 '코드 품질개선, 리포지터리 차원의 코드 일관성 향상, 엔지니어 전문성 향상에서 절약하는 장기적인 비용'을 의식적으로 맞바꾸는 제도
  - 정적분석 도구를 활용하여 가독성 개선 제안 중 상당수를 자동으로 검출하여 설명과 함께 안내해주려 함


> 생각해볼 것들
> - go link 를 회사에 개발해 볼 수 있을까?
> - kudos 채널을 만들어 볼까?

----

## Chapter 4. 공정 사회를 위한 엔지니어링
> 핵심 메시지
> - 다양한 계층의 사용자를 위한 제품을 설계할 때 엔지니어가 짊어져야 할 책임
> - 조직이 다양성을 포용하여 모든 사람을 위하는 시스템을 설계하고 의도치 않게 사용자에게 상처 주는 일이 없게끔 하려면

### 편견은 피할 수 없다
- 모든 사람은 편견을 지니고 있다
- 구글 엔지니어의 구성 비 (대부분 남성, 백인 혹은 아시아인 -> 사용자들을 대표하지 못한다)
- 소프트웨어 엔지니어링 조직 자체의 인적 구성을 제품이 목표하는 시장의 인적 구성과 비슷해지도록

### 사내 이동시 지원자의 성과 등급을 보여주는 기능
- 기존의 평가가 향후 성과를 예측할 수 있나?
- 성과 평가가 다음 관리자에게 편견을 주지 않나?
- 성과 평가 점수가 회사 전체적으로 표준화된 것인가?
- `등급은 특정 시기의 성과 평가에 중요한 수단인 것은 사실이지만, 미래의 성과를 예견해주지 못했다`

### 가치 vs 결과
- 자신을 솔직하게 바라보고 성찰하자
- 모두를 위해 만들지 말자. 모두와 '함께' 만들자
- 제품을 이용하기 가장 어려운 이들을 위해 설계하자
- 가정하지 말고, 시스템 전반의 공정성을 측정하자
- 변할 수 있다

> 생각해볼 것들
> - 사내 이동시 지원자의 성과등급을 보여줄 필요 없다

## Chapter 5. 팀 이끌기
> 핵심 메시지
> - 관리자(mamager)는 사람을 이끌고 테크리드(Tech lead)는 기술 관련 책임을 진다
> - 개인기여자 (Individual contributor)에서 관리자, Tech lead로

### 관리자와 테크리드 (혹은 둘 다)
- 엔지니어링 매니저 : 구성원의 성과 performance, 생산성 productivity, 행복 happiness을 책임지며, 제품의 사업적 요구를 충족시켜야 한다
- 테크리드 : 기술 결정, 아키텍처, 우선순위, 성능, 프로젝트 관리를 책임진다. 팀 관리자의 직속인 경우가 많다. 대부분의 테크리드는 개인기여자이기도 함
- 테크리드 매니저 : 소규모 팀은 두 역할을 한명이 맡음. 팀이 커지면 보통 1명씩으로 분리

### 개인 기여자에서 리드로
- '오늘은 한 일이 하나도 없군'? 바나나를 재배하면서 사과를 세는 함정에 빠지지 마세요.
- '무엇보다도 관리하려는 충동을 이겨내야 해요'
  - 겸손, 존중, 신뢰의 분위기를 조성, 팀원이 혼자서 제거할 수 없는 관료적 장애물을 치워주고, 팀이 합의에 이르도록 도와주고, 누군가 늦게까지 야근할때 저녁을 사주고...
  - 리더가 행하는 '관리'는 오직 팀의 기술적, 사회적 건강관리 뿐이다.

### 엔지니어링 매니저
- `전통적인 관리자는 일을 '어떻게 how' 처리할지를 고민하는 반면, 훌륭한 관리자는 '무슨 what'일을 처리할지를 고민합니다. (그리고 어떻게는 팀을 믿고 맡깁니다)`

### 안티패턴
- 만만한 사람 고용하기
- 저성과자 방치하기 : `"모든 치아를 공평하게 대해야 하지만, 때로는 치과의사가 되어야 한다네"`
- 사람 문제 무시하기 : 관리자는 `기술적 문제`와 `사회적 문제`를 신경써야 한다.
- 만인의 친구되기 : 리딩과 우정을 혼동하지 말라
- `적합한 사람을 찾는데 드는 비용은 애초에 뽑지 말았어야 할 직원을 관리하는 비용에 비하면 아무것도 아니다`
- 팀을 어린이처럼 대하기 : `사람들은 자신을 대하는 방식대로 행동하는 경향이 있다`. 믿어야 믿음직한 행동을 한다.

### 올바른 패턴
- 자존심 버리기
- 마음 다스리기 : 
  - 더 많은 사람을 이끌수록 감정은 억누르고 평정심을 유지해야 합니다. 
  - `CEO가 조금만 움직여도 예닐곱 단계 아래에 있는 불운한 사원 바퀴들은 정신없이 돌게 됩니다`
  = 리더는 항상 무대 위에 있다고 생각하라.
  - 큰 문제가 있다고 찾아온 직원에게 "문제가 정확히 무엇인지 묻는다"
- 팀 리더가 하는 가장 일반적인 일은 합의를 이끌어 내는 것이다.
- 여러분이 장애물을 치울 수 있고 기꺼이 그러길 원한다는 사실을 팀원 모두가 인지하도록 만들어야 한다.
- 정확한 답을 알고 있기보다 올바른 사람을 알고 있을 때의 가치가 크다.
- 멘토되기 : 멘티가 배우는 데 쓰는 시간과 제품 개발에 기여하는 시간의 균형을 잘 잡아줘야 한다.
- 명확한 목표 세우기 : 우선순위를 명확히 설정해놓고, 구체적으로 무엇을 택하고 무엇을 버려야할지는 팀이 스스로 정하도록 적시에 도와야 한다.
- 정직하기 : '답은 알지만 내 마음대로 얘기해줄 수 없다' '모른다'
- `칭찬 샌드위치를 사용하지 말 것을 강력하게 권한다`
- 팀원들이 행복해 하는지 주기적으로 확인해야 한다

### 그 외의 조언과 요령
- 위임하되, 곤란한 일은 직접 처리하자
- 나를 대신할 사람을 찾자
- `사람의 문제는 무시하지 말고 빨리 조치를 취하자` (낮은 기술수준, 의욕이 낮은 상태, 겸손/존중 부족)
- `팀이 잘하고 있으면 칭찬하자`
- 쉽게 되돌릴 수 있는 일에는 '해보세요'라고 말하자


### 사람은 식물과 같다
- 동기부여와 방향지시 두가지를 사용하라
- 내적동기 : 자율성, 숙련(성장), 목적(의미) 
> 성과, 성장, 의미 중 성과는 외적 동기, 성장과 의미는 내적동기다. 내적동기에 하나 더 중요한 것은 자율성이다.

> 생각해볼 것들
> - 행복을 체크해보자


## Chapter 6. 성장하는 조직 이끌기
> 핵심 메시지
> - 팀 하나를 이끌다가 여러 팀을 이끌게 되는 과정
> - 3A 리더십

### 늘 결정하라 (Always Be Deciding)
- 트레이드 오프
  - 눈가리개 찾기 > 트레이드오프 이해 > 지속적인 재조정
  - '트레이드오프의 지속적인 재조정'을 프로세스에 녹이지 않으면 팀은 완벽한 해법을 찾으려는 함정에 빠진다.
  - 웹검색 트레이드 오프 : 삼각 트레이드 오프 - `좋게(품질), 빠르게(지연), 저렴하게(용량) 중 두 개만 선택해!`
> 결정에 관련된 중요한 요인 두가지
> - 트레이드 오프
> - one-way or two-way door
>   - one-way : 신중하게 결정하고 위험을 최소화 하기
>   - two-way : 빠르게 시도하고 배우기

### 늘 떠나라 (Always Be Leaving)
- `리더는 문제를 풀어줄 뿐 아니라 맡은 조직이 리더 없이 '스스로' 문제를 풀 수 있게 유도해야 한다` - `자생력을 갖춘 팀`
- 자생력을 갖춘 팀 만들기 : 문제공간 분할 > 하위문제 위임 > 반복
- 관찰과 경청 95%, 절묘하고 시의적절한 개입 5% 이것이 좋은 관리입니다.
- `끊임없이 경로를 수정해주는 대신 한 주의 대부분을 세심히 관찰하고 경청하는데 씁니다. 한 주가 끝나갈 즈음 분필을 들고 수정할 정확한 위치를 살짝 표시해주는 거죠. 작지만 아주 중요한 '터치'로 경로를 조정해주는 겁니다`
- `시의적절한 개입 vs 스스로 경로를 바꾸는 힘 (회고)`
- `팀에는 문제를 맡겨야 한다. 특정 제품을 맡기지 말라`
> 자생력 있는 팀의 중요한 요인 세가지
> - 위임 : 95% 관찰, 5% 개입
> - 회고 : 스스로 발전하는 팀
> - 미션 : 특정 제품과 모듈을 책임지는 팀이 아니라 '문제'를 책임지고 해결하는 팀

### 늘 확장하라 (Always Be Scaling)
- 규모 확장 과정에서 개인도 함께 확장해나가는 방법
- `자신의 시간, 집중력, 에너지`
- `중요한 일 vs 급한 일 = 주도하기 vs 반응하기`
- 중요한 일 (주도할 일)에 집중하는 방법
  - 위임
  - 정기적인 시간을 확보하기 (캘린더)
  - 나만의 추적 시스템 만들기
  - 공 떨어뜨리기 (가장 소중한 20%에만 집중하고 나머지는 버리기)
- 에너지 관리하기
  - 진짜 휴가 떠나기
  - 일과 단절되는 시간 갖기
  - 진짜 주말 보내기
  - 매일 매일 휴식하기
  -` 안좋은 날은 아무것도 하지 않기`

> 생각해볼 것들
> - 시스템 운영의 삼각 트레이드오프 적용 (속도, 품질, 비용)
> - 지금의 팀 구조를 문제 기반으로 변경할 수 있을까?
> - '압축' 단계에 필요한 것들 정의해보기

## Chapter 7. 엔지니어링 생산성 측정하기
> 핵심 메시지
> - 엔지니어링 생산성 자체에 집중하는 전문가 팀을 꾸려두면 값진 통찰을 얻을 수 있음

### 엔지니어링 생산성을 측정하는 이유
- 조직이 두배 커지면 소통 비용은 제곱으로 늘어난다
- 사업을 두배 늘릴때 사람수를 늘리지 말고, 사람의 생산성을 늘리자

### 측정할 가치가 있는가?
- 어떤 결과를 기대하는가? (편향)
- 기대한 결과를 뒷받침한다면 어떤 조치를, 반대라면 어떤 조치를 취할 것인가?
- 결정권자가 누구인가?

### 지표선정 - GSM(Goal/Signal/Metric)

### Goal - 구글의 생산성 5개 측면 : QUANTS
- `생산성에 5개의 측면(트레이드오프)이 있으며, 하나에 집중하면  나머지 측면이 무시될 수 있음을 인지해야 한다`
- Quality of code
- Attention from engineers
- iNtellectual complexity
- Tempo and velocity
- Satisfaction

### 기타
- 구글도 코드품질에 대해 엔지니어들에게 스스로 평가하라고만 요청하고 정량적인 측정은 포기했다
- 정량적 지표는 신뢰와 확장성에서 의미있으나 왜 그런일이 일어났는지를 설명해주지 못한다
- 정성적 연구만이 이런 정보를 제공해주며 이런 맥락정보를 통해서만 프로세스를 개선하기 위해 취해야 할 다음 단계가 무엇인지 말해줄 수 있다

- `회상편향` : 특별히 관심있거나 실망한 사건만 회상
- `최신편향` : 최근 경험을 떠올릴 가능성이 높다
- `표본편향` : 표본이 특정 유형에 집중되는 현상

- `도구의 지원 없이 엔지니어들에게 업무 프로세스나 사고방시을 바꾸라고 요구하는 것은 좋지 않다`
- 도구, 보상, 워크플로우(프로세스), 문화

> 생각해볼 것들
> - ㅁㅁ
