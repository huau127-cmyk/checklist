<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>우리 아이 발달 체크리스트 | 언어행동연구소 온유</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Noto+Serif+KR:wght@300;400;500;600;700&family=Noto+Sans+KR:wght@300;400;500;700&display=swap" rel="stylesheet">
<style>
  :root {
    --pink: #D97B8E;
    --pink-light: #F0C4CE;
    --pink-pale: #FAF0F2;
    --yellow: #E8B84B;
    --yellow-light: #F7E4A8;
    --yellow-pale: #FFFBF0;
    --purple: #8B7AB8;
    --purple-light: #C5BCE0;
    --purple-pale: #F4F2FA;
    --ivory: #FAF8F4;
    --ivory-dark: #EDE9E0;
    --charcoal: #2C2A27;
    --gray: #7A776F;
    --gray-light: #B8B3A8;
    --serif: 'Noto Serif KR', serif;
    --sans: 'Noto Sans KR', sans-serif;
  }
  * { margin: 0; padding: 0; box-sizing: border-box; }
  html { scroll-behavior: smooth; }
  body { background: var(--ivory); color: var(--charcoal); font-family: var(--sans); min-height: 100vh; }
  .header { background: white; border-bottom: 1px solid var(--ivory-dark); padding: 20px 24px; text-align: center; position: sticky; top: 0; z-index: 50; }
  .header-brand { font-size: 11px; font-weight: 600; letter-spacing: 1.5px; color: var(--pink); text-transform: uppercase; margin-bottom: 4px; }
  .header-title { font-family: var(--serif); font-size: 20px; font-weight: 600; color: var(--charcoal); letter-spacing: -0.3px; }
  .intro { padding: 32px 24px 0; max-width: 640px; margin: 0 auto; }
  .intro-card { background: white; border-radius: 20px; padding: 24px 24px 20px; border: 1px solid var(--ivory-dark); margin-bottom: 24px; }
  .intro-label { font-size: 11px; font-weight: 600; letter-spacing: 1px; color: var(--purple); text-transform: uppercase; margin-bottom: 8px; }
  .intro-text { font-size: 14px; line-height: 1.8; color: var(--gray); font-weight: 300; }
  .intro-note { display: flex; gap: 10px; align-items: flex-start; background: var(--pink-pale); border: 1px solid var(--pink-light); border-radius: 12px; padding: 14px 16px; font-size: 12px; color: var(--pink); line-height: 1.6; font-weight: 400; margin-top: 14px; }
  .intro-note::before { content: '⚠️'; flex-shrink: 0; }
  .age-tabs-wrap { padding: 0 24px; max-width: 640px; margin: 0 auto 8px; }
  .age-tabs { display: flex; gap: 8px; overflow-x: auto; padding-bottom: 4px; scrollbar-width: none; }
  .age-tabs::-webkit-scrollbar { display: none; }
  .age-tab { flex-shrink: 0; background: white; border: 1.5px solid var(--ivory-dark); border-radius: 50px; padding: 10px 18px; font-family: var(--sans); font-size: 13px; font-weight: 500; color: var(--gray); cursor: pointer; transition: all 0.2s; white-space: nowrap; }
  .age-tab:hover { border-color: var(--pink-light); color: var(--pink); }
  .age-tab.active { background: var(--pink); border-color: var(--pink); color: white; box-shadow: 0 4px 14px rgba(217,123,142,0.35); }
  .checklist-wrap { padding: 16px 24px 120px; max-width: 640px; margin: 0 auto; }
  .age-section { display: none; }
  .age-section.active { display: block; animation: fadeIn 0.3s ease; }
  @keyframes fadeIn { from { opacity: 0; transform: translateY(8px); } to { opacity: 1; transform: translateY(0); } }
  .age-header { margin-bottom: 20px; }
  .age-header-badge { display: inline-flex; align-items: center; gap: 8px; background: var(--purple-pale); border: 1px solid var(--purple-light); padding: 6px 14px; border-radius: 50px; font-size: 11px; font-weight: 600; color: var(--purple); letter-spacing: 0.5px; margin-bottom: 12px; }
  .age-header-title { font-family: var(--serif); font-size: 22px; font-weight: 600; line-height: 1.3; letter-spacing: -0.3px; margin-bottom: 8px; }
  .age-header-desc { font-size: 13px; color: var(--gray); line-height: 1.7; font-weight: 300; }
  .domain-block { margin-bottom: 24px; }
  .domain-label { display: flex; align-items: center; gap: 8px; font-size: 13px; font-weight: 600; margin-bottom: 12px; padding: 10px 14px; border-radius: 10px; }
  .domain-label.d-lang { background: var(--pink-pale); color: var(--pink); }
  .domain-label.d-social { background: var(--yellow-pale); color: #9A7520; }
  .domain-label.d-behavior { background: var(--purple-pale); color: var(--purple); }
  .domain-label.d-cognitive { background: rgba(100,160,120,0.1); color: #3A7A50; }
  .domain-label.d-motor { background: rgba(80,140,200,0.1); color: #2A6A9A; }
  .domain-label.d-self { background: rgba(210,120,80,0.1); color: #B85A30; }
  .domain-dot { width: 8px; height: 8px; border-radius: 50%; flex-shrink: 0; }
  .d-lang .domain-dot { background: var(--pink); }
  .d-social .domain-dot { background: var(--yellow); }
  .d-behavior .domain-dot { background: var(--purple); }
  .d-cognitive .domain-dot { background: #3A7A50; }
  .d-motor .domain-dot { background: #2A6A9A; }
  .d-self .domain-dot { background: #B85A30; }
  .domain-ref { font-size: 11px; color: var(--gray-light); font-weight: 300; margin-top: -6px; margin-bottom: 14px; padding-left: 2px; }
  .check-item { background: white; border-radius: 16px; border: 1.5px solid var(--ivory-dark); padding: 16px 16px 14px; margin-bottom: 10px; transition: border-color 0.2s, box-shadow 0.2s; }
  .check-item.answered-yes { border-color: var(--pink-light); background: var(--pink-pale); }
  .check-item.answered-no { border-color: var(--ivory-dark); background: var(--ivory); }
  .item-top { display: flex; gap: 12px; align-items: flex-start; margin-bottom: 10px; }
  .item-badges { display: flex; gap: 6px; flex-wrap: wrap; flex-shrink: 0; margin-top: 2px; }
  .item-badge { font-size: 10px; font-weight: 600; padding: 3px 8px; border-radius: 50px; letter-spacing: 0.3px; white-space: nowrap; }
  .badge-month { background: var(--purple-pale); color: var(--purple); }
  .badge-common { background: var(--ivory-dark); color: var(--gray); }
  .badge-alert { background: rgba(220,80,80,0.1); color: #c04040; }
  .item-text { font-size: 15px; font-weight: 500; line-height: 1.5; color: var(--charcoal); flex: 1; }
  .item-sub { font-size: 12px; color: var(--gray); line-height: 1.6; font-weight: 300; padding-left: 0; margin-bottom: 12px; }
  .item-actions { display: flex; gap: 8px; }
  .yn-btn { flex: 1; padding: 10px; border-radius: 10px; border: 1.5px solid var(--ivory-dark); background: white; font-family: var(--sans); font-size: 13px; font-weight: 500; color: var(--gray); cursor: pointer; transition: all 0.15s; display: flex; align-items: center; justify-content: center; gap: 6px; }
  .yn-btn:hover { transform: translateY(-1px); }
  .yn-btn.yes-btn:hover { border-color: var(--pink-light); color: var(--pink); }
  .yn-btn.no-btn:hover { border-color: var(--gray-light); color: var(--charcoal); }
  .yn-btn.selected-yes { background: var(--pink); border-color: var(--pink); color: white; box-shadow: 0 3px 10px rgba(217,123,142,0.3); }
  .yn-btn.selected-no { background: var(--charcoal); border-color: var(--charcoal); color: white; }
  .result-panel { position: fixed; bottom: 0; left: 0; right: 0; background: white; border-top: 1px solid var(--ivory-dark); padding: 16px 24px; z-index: 40; box-shadow: 0 -8px 30px rgba(44,42,39,0.08); }
  .result-inner { max-width: 640px; margin: 0 auto; display: flex; align-items: center; gap: 16px; }
  .result-counts { display: flex; gap: 16px; flex: 1; }
  .result-count-item { display: flex; align-items: center; gap: 8px; }
  .count-dot { width: 10px; height: 10px; border-radius: 50%; flex-shrink: 0; }
  .count-dot.yes { background: var(--pink); }
  .count-dot.no { background: var(--gray-light); }
  .count-label { font-size: 12px; color: var(--gray); }
  .count-num { font-family: var(--serif); font-size: 20px; font-weight: 600; line-height: 1; }
  .count-num.yes { color: var(--pink); }
  .count-num.no { color: var(--charcoal); }
  .result-bar-wrap { flex: 2; }
  .result-bar-label { font-size: 11px; color: var(--gray); margin-bottom: 6px; }
  .result-bar-bg { height: 8px; background: var(--ivory-dark); border-radius: 50px; overflow: hidden; }
  .result-bar-fill { height: 100%; background: var(--pink); border-radius: 50px; transition: width 0.4s ease; }
  .result-cta-btn { background: var(--pink); color: white; border: none; border-radius: 50px; padding: 12px 20px; font-family: var(--sans); font-size: 13px; font-weight: 600; cursor: pointer; transition: all 0.2s; white-space: nowrap; flex-shrink: 0; }
  .result-cta-btn:hover { background: #c46a7c; transform: translateY(-1px); }
  .modal-overlay { display: none; position: fixed; inset: 0; background: rgba(44,42,39,0.5); z-index: 100; align-items: flex-end; justify-content: center; }
  .modal-overlay.open { display: flex; }
  .modal { background: white; border-radius: 28px 28px 0 0; padding: 32px 24px 40px; width: 100%; max-width: 640px; animation: slideUp 0.35s ease; max-height: 90vh; overflow-y: auto; }
  @keyframes slideUp { from { transform: translateY(100%); } to { transform: translateY(0); } }
  .modal-handle { width: 40px; height: 4px; background: var(--ivory-dark); border-radius: 2px; margin: 0 auto 24px; }
  .modal-title { font-family: var(--serif); font-size: 24px; font-weight: 600; margin-bottom: 8px; letter-spacing: -0.3px; }
  .modal-subtitle { font-size: 14px; color: var(--gray); margin-bottom: 28px; font-weight: 300; }
  .modal-score-ring { display: flex; align-items: center; gap: 24px; background: var(--ivory); border-radius: 20px; padding: 24px; margin-bottom: 24px; }
  .ring-wrap { position: relative; width: 80px; height: 80px; flex-shrink: 0; }
  .ring-svg { width: 80px; height: 80px; transform: rotate(-90deg); }
  .ring-bg { fill: none; stroke: var(--ivory-dark); stroke-width: 8; }
  .ring-fill { fill: none; stroke: var(--pink); stroke-width: 8; stroke-linecap: round; transition: stroke-dashoffset 0.6s ease; }
  .ring-label { position: absolute; inset: 0; display: flex; flex-direction: column; align-items: center; justify-content: center; }
  .ring-num { font-family: var(--serif); font-size: 18px; font-weight: 700; color: var(--pink); line-height: 1; }
  .ring-sub { font-size: 10px; color: var(--gray); margin-top: 2px; }
  .score-detail { flex: 1; }
  .score-detail-title { font-family: var(--serif); font-size: 16px; font-weight: 600; margin-bottom: 6px; }
  .score-detail-desc { font-size: 13px; color: var(--gray); line-height: 1.7; font-weight: 300; }
  .domain-results { margin-bottom: 28px; }
  .domain-result-item { display: flex; align-items: center; gap: 12px; padding: 12px 0; border-bottom: 1px solid var(--ivory-dark); }
  .domain-result-item:last-child { border-bottom: none; }
  .domain-result-name { font-size: 13px; font-weight: 500; width: 80px; flex-shrink: 0; }
  .domain-mini-bar { flex: 1; height: 6px; background: var(--ivory-dark); border-radius: 50px; overflow: hidden; }
  .domain-mini-fill { height: 100%; border-radius: 50px; transition: width 0.5s ease; }
  .domain-result-count { font-size: 12px; color: var(--gray); width: 40px; text-align: right; }
  .modal-advice { background: var(--purple-pale); border: 1px solid var(--purple-light); border-radius: 16px; padding: 20px; margin-bottom: 24px; }
  .advice-label { font-size: 11px; font-weight: 700; letter-spacing: 1px; color: var(--purple); text-transform: uppercase; margin-bottom: 8px; }
  .advice-text { font-size: 14px; line-height: 1.8; color: var(--charcoal); font-weight: 400; }
  .modal-cta { display: flex; flex-direction: column; gap: 10px; }
  .modal-btn-secondary { display: block; width: 100%; background: var(--ivory); color: var(--charcoal); border: 1.5px solid var(--ivory-dark); border-radius: 14px; padding: 14px; font-family: var(--sans); font-size: 14px; font-weight: 500; cursor: pointer; text-align: center; transition: all 0.2s; }
  .modal-btn-secondary:hover { border-color: var(--pink-light); color: var(--pink); }
  .consult-box { margin-bottom: 20px; border-radius: 16px; overflow: hidden; border: 1.5px solid var(--ivory-dark); }
  .consult-urgent { display: flex; gap: 12px; align-items: flex-start; background: rgba(220,60,60,0.07); border-bottom: 1.5px solid rgba(220,60,60,0.15); padding: 16px 18px; }
  .consult-urgent-icon { font-size: 18px; flex-shrink: 0; margin-top: 1px; }
  .consult-urgent-title { font-size: 13px; font-weight: 700; color: #c04040; margin-bottom: 3px; }
  .consult-urgent-desc { font-size: 12px; color: #c04040; line-height: 1.5; font-weight: 400; opacity: 0.85; }
  .consult-main { background: white; padding: 20px 18px; }
  .consult-step { display: flex; gap: 14px; align-items: flex-start; }
  .consult-step-num { width: 24px; height: 24px; flex-shrink: 0; background: var(--pink); color: white; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 12px; font-weight: 700; margin-top: 1px; }
  .consult-step-body { flex: 1; }
  .consult-step-title { font-size: 14px; font-weight: 600; color: var(--charcoal); margin-bottom: 5px; line-height: 1.4; }
  .consult-step-desc { font-size: 12px; color: var(--gray); line-height: 1.7; font-weight: 300; }
  .consult-divider { height: 1px; background: var(--ivory-dark); margin: 16px 0; }
  .consult-link { display: inline-block; margin-top: 10px; background: var(--pink); color: white; font-size: 13px; font-weight: 600; padding: 10px 18px; border-radius: 50px; text-decoration: none; transition: all 0.2s; }
  .consult-link:hover { background: #c46a7c; transform: translateY(-1px); }
  .modal-close { position: absolute; top: 20px; right: 20px; width: 32px; height: 32px; background: var(--ivory); border: none; border-radius: 50%; display: flex; align-items: center; justify-content: center; cursor: pointer; font-size: 16px; color: var(--gray); transition: background 0.2s; }
  .modal-close:hover { background: var(--ivory-dark); }
  .onyu-footer { display: flex; align-items: center; justify-content: space-between; font-size: 11px; color: var(--gray-light); padding: 0 24px 12px; max-width: 640px; margin: 0 auto; }
</style>
</head>
<body>
<div class="header">
  <div class="header-brand">언어행동연구소 온유</div>
  <div class="header-title">우리 아이 발달 체크리스트</div>
</div>

<div class="intro">
  <div class="intro-card">
    <div class="intro-label">사용 방법</div>
    <div class="intro-text">
      아이의 연령대를 선택하고, 각 항목에 <strong>예</strong>(해당됨) 또는 <strong>아니오</strong>(해당 없음)로 답해 주세요.
      <strong>같은 영역에서 2개 이상 해당되거나, 언어 퇴행 항목이 해당되면</strong> 전문가 상담을 권장합니다.
    </div>
    <div class="intro-note">이 체크리스트는 선별 도구이며 진단을 대체하지 않습니다. CDC 발달 이정표, DSM-5, M-CHAT-R/F 기준을 참고했습니다.</div>
  </div>
</div>

<div class="age-tabs-wrap">
  <div class="age-tabs" id="ageTabs">
    <button class="age-tab active" data-age="18-36">18–36개월</button>
    <button class="age-tab" data-age="36-48">36–48개월</button>
    <button class="age-tab" data-age="48-60">만 4–5세</button>
    <button class="age-tab" data-age="60-72">만 6–7세</button>
    <button class="age-tab" data-age="school">만 8–9세</button>
  </div>
</div>

<div class="checklist-wrap" id="checklistWrap"></div>

<div class="result-panel">
  <div class="result-inner">
    <div class="result-counts">
      <div class="result-count-item">
        <div class="count-dot yes"></div>
        <div><div class="count-label">해당됨</div><div class="count-num yes" id="yesCount">0</div></div>
      </div>
      <div class="result-count-item">
        <div class="count-dot no"></div>
        <div><div class="count-label">응답함</div><div class="count-num no" id="totalCount">0</div></div>
      </div>
    </div>
    <div class="result-bar-wrap">
      <div class="result-bar-label" id="barLabel">항목에 응답해 주세요</div>
      <div class="result-bar-bg"><div class="result-bar-fill" id="barFill" style="width:0%"></div></div>
    </div>
    <button class="result-cta-btn" id="showResultBtn">결과 보기</button>
  </div>
</div>

<div class="modal-overlay" id="modalOverlay">
  <div class="modal" id="modal" style="position:relative">
    <button class="modal-close" id="modalClose">✕</button>
    <div class="modal-handle"></div>
    <div class="modal-title" id="modalTitle">체크리스트 결과</div>
    <div class="modal-subtitle" id="modalSubtitle"></div>

    <div class="modal-score-ring">
      <div class="ring-wrap">
        <svg class="ring-svg" viewBox="0 0 80 80">
          <circle class="ring-bg" cx="40" cy="40" r="32"/>
          <circle class="ring-fill" id="ringFill" cx="40" cy="40" r="32" stroke-dasharray="201" stroke-dashoffset="201"/>
        </svg>
        <div class="ring-label">
          <div class="ring-num" id="ringNum">0</div>
          <div class="ring-sub">해당</div>
        </div>
      </div>
      <div class="score-detail">
        <div class="score-detail-title" id="scoreTitle"></div>
        <div class="score-detail-desc" id="scoreDesc"></div>
      </div>
    </div>

    <div class="domain-results" id="domainResults"></div>

    <div class="modal-advice" id="modalAdvice">
      <div class="advice-label">박소현 BCBA의 안내</div>
      <div class="advice-text" id="adviceText"></div>
    </div>

    <div class="consult-box" id="consultBox" style="display:none">
      <div class="consult-urgent" id="consultUrgent" style="display:none">
        <span class="consult-urgent-icon">🚨</span>
        <div>
          <div class="consult-urgent-title">'언어 퇴행' 항목이 해당됩니다</div>
          <div class="consult-urgent-desc">1개라도 해당된다면 지금 바로 전문가와 확인하세요.</div>
        </div>
      </div>
      <div class="consult-main">
        <div class="consult-step">
          <div class="consult-step-num">1</div>
          <div class="consult-step-body">
            <div class="consult-step-title">소아정신과 진료를 받아보세요</div>
            <div class="consult-step-desc">발달 선별과 공식 진단은 소아정신과에서 받는 것이 가장 정확합니다. 진단 여부와 관계없이 지원이 필요하다면 치료를 시작할 수 있어요.</div>
          </div>
        </div>
        <div class="consult-divider"></div>
        <div class="consult-step">
          <div class="consult-step-num">2</div>
          <div class="consult-step-body">
            <div class="consult-step-title">언어행동연구소 온유에 상담 문의하세요</div>
            <div class="consult-step-desc">어디서 시작해야 할지 모르겠어도 괜찮아요. 지금 고민하는 것을 먼저 이야기해 주세요. 아이에게 맞는 방향을 함께 찾아드립니다.</div>
            <a href="http://pf.kakao.com/_xhGDyn" class="consult-link" target="_blank">💬 카카오톡 채널로 상담 문의 →</a>
          </div>
        </div>
      </div>
    </div>

    <div class="modal-cta">
      <button class="modal-btn-secondary" id="resetBtn">다시 체크하기</button>
    </div>
  </div>
</div>

<div class="onyu-footer"><span>@onyou_abalab</span><span>언어행동연구소 온유</span></div>

<script>
const DATA = {
  "18-36": {
    label: "만 18–36개월", title: "만 18–36개월 발달 체크리스트", desc: "언어와 사회성이 빠르게 발달하는 중요한 시기입니다.",
    domains: [
      { id: "lang", name: "언어 발달", type: "d-lang", ref: "CDC Developmental Milestones 2022 · DSM-5-TR (2022) 언어 퇴행 신호", items: [
        { id: "l1", badge: "18개월", text: "의미 있는 단어가 거의 없다", sub: '"엄마", "아빠", "줘" 등 의도를 담은 말 없음' },
        { id: "l2", badge: "18개월", text: "원하는 것을 말로 요청하지 않는다", sub: '"더", "줘", "안 돼" 같은 기능적 표현이 없음' },
        { id: "l3", badge: "24개월", text: "두 단어를 붙여서 말하지 못한다", sub: '"엄마 줘", "물 더" 같은 조합 없음' },
        { id: "l4", badge: "공통", text: "한 번 쓰던 말이 갑자기 줄거나 사라졌다", sub: "즉시 전문가와 확인이 필요한 신호", alert: true },
        { id: "l5", badge: "공통", text: "말은 있는데 원하는 것을 표현하는 데 쓰지 않는다", sub: "소리나 단어는 있지만 요청, 대화 목적으로 쓰지 않음" },
      ]},
      { id: "social", name: "사회적 상호작용", type: "d-social", ref: "M-CHAT-R/F 공식 항목 기반 (Robins et al., 2014, Pediatrics)", items: [
        { id: "s1", badge: "공통", text: "이름을 불러도 반응이 없거나 일관되지 않는다" },
        { id: "s2", badge: "공통", text: "눈 맞춤이 거의 없다" },
        { id: "s3", badge: "공통", text: "손가락으로 원하는 걸 가리키지 않는다", sub: "보여주거나 요청하기 위한 pointing 없음" },
        { id: "s4", badge: "공통", text: "흥미로운 걸 발견해도 엄마에게 보여주려 하지 않는다" },
        { id: "s5", badge: "공통", text: "다른 아이들에게 관심이 없다" },
      ]},
      { id: "behavior", name: "행동 패턴", type: "d-behavior", ref: "DSM-5-TR (2022) 제한적·반복적 행동 기준 (criterion B)", items: [
        { id: "b1", badge: "공통", text: "특정 루틴이나 순서가 바뀌면 또래보다 훨씬 강하게 반응한다" },
        { id: "b2", badge: "공통", text: "손 흔들기, 몸 흔들기, 뱅글뱅글 돌기가 반복된다", sub: "달래거나 주의를 끌어도 멈추지 않는 경우" },
        { id: "b3", badge: "공통", text: "장난감을 기능대로 갖고 놀지 않는다", sub: "줄 세우기, 특정 부분만 반복 조작 등" },
        { id: "b4", badge: "공통", text: "특정 소리, 촉감, 빛에 또래보다 훨씬 예민하거나 전혀 반응하지 않는다" },
      ]}
    ]
  },
  "36-48": {
    label: "만 36–48개월", title: "만 36–48개월 발달 체크리스트", desc: "문장으로 소통하고 또래와 놀기 시작하는 시기입니다.",
    domains: [
      { id: "lang", name: "언어 발달", type: "d-lang", ref: "CDC Developmental Milestones 2022 · DSM-5-TR (2022) 언어 퇴행 신호", items: [
        { id: "l1", badge: "36개월", text: "세 단어 이상 붙여서 말하지 않는다", sub: '"엄마 물 줘", "나 더 먹고 싶어" 같은 말 없음' },
        { id: "l2", badge: "36개월", text: "자기 이름, 나이를 말하지 못한다" },
        { id: "l3", badge: "36개월", text: '그림책 보며 "뭐 해?" 물으면 대답하지 못한다' },
        { id: "l4", badge: "48개월", text: '"왜", "어디", "누가" 같은 질문에 대답하지 못한다' },
        { id: "l5", badge: "공통", text: "혼자 말은 하는데 대화가 이어지지 않는다", sub: "질문하면 엉뚱한 말을 하거나 무시함" },
        { id: "l6", badge: "공통", text: "한 번 쓰던 말이 갑자기 줄거나 사라졌다", sub: "즉시 전문가와 확인이 필요한 신호", alert: true },
      ]},
      { id: "social", name: "사회적 상호작용", type: "d-social", ref: "M-CHAT-R/F 공식 항목 기반 (Robins et al., 2014, Pediatrics)", items: [
        { id: "s1", badge: "공통", text: "또래 옆에 있어도 혼자만 논다", sub: "같이 놀자 해도 반응이 없음" },
        { id: "s2", badge: "공통", text: "소꿉놀이, 인형놀이 등 흉내 내는 놀이를 하지 않는다" },
        { id: "s3", badge: "공통", text: "친구가 다쳐서 울어도 쳐다보지 않는다" },
        { id: "s4", badge: "공통", text: "슬픈 상황에서 웃거나 기쁜 상황에서 우는 경우가 자주 있다" },
        { id: "s5", badge: "공통", text: "줄 서기, 순서 지키기를 또래보다 훨씬 힘들어한다" },
      ]},
      { id: "behavior", name: "행동 패턴", type: "d-behavior", ref: "DSM-5-TR (2022) 제한적·반복적 행동 기준 (criterion B)", items: [
        { id: "b1", badge: "공통", text: "특정 장난감이나 주제에만 집착하고 다른 것으로 넘어가지 못한다" },
        { id: "b2", badge: "공통", text: "작은 변화에도 소리 지르거나 바닥에 드러눕는 등 또래보다 훨씬 강하게 반응한다" },
        { id: "b3", badge: "공통", text: "TV 대사나 들은 말을 상황과 관계없이 반복해서 말한다" },
        { id: "b4", badge: "공통", text: "특정 소리, 옷 감촉, 음식 냄새에 또래보다 훨씬 예민하거나 전혀 반응하지 않는다" },
      ]},
      { id: "cognitive", name: "인지 발달", type: "d-cognitive", ref: "CDC Developmental Milestones 2022 · Conners Early Childhood", items: [
        { id: "c1", badge: "36개월", text: "3~4조각 퍼즐을 완성하지 못한다" },
        { id: "c2", badge: "36개월", text: "빨강, 파랑 등 기본 색깔을 구별하지 못한다" },
        { id: "c3", badge: "48개월", text: '"신발 신고, 가방 들고, 문 앞에 서" 같은 세 가지 지시를 순서대로 하지 못한다' },
        { id: "c4", badge: "48개월", text: "하나, 둘, 셋 이상 세지 못한다" },
        { id: "c5", badge: "공통", text: "그림책을 읽어줘도 이야기를 따라가지 못하고 금방 딴짓을 한다" },
      ]},
      { id: "selfregulation", name: "자기조절", type: "d-self", ref: "DSM-5-TR (2022) · Conners Early Childhood", items: [
        { id: "r1", badge: "공통", text: "작은 변화에도 소리 지르거나 바닥에 드러눕는 등 또래보다 훨씬 강하게 반응한다" },
        { id: "r2", badge: "공통", text: "좋아하는 활동도 3~5분 이상 이어가지 못한다" },
        { id: "r3", badge: "공통", text: '"안 돼", "위험해" 해도 하던 행동을 멈추지 않는다' },
        { id: "r4", badge: "공통", text: "어린이집이나 유치원에서 매일 심하게 울거나 배가 아프다고 한다" },
      ]}
    ]
  },
  "48-60": {
    label: "만 4–5세", title: "만 4–5세 발달 체크리스트", desc: "유치원 생활이 본격 시작되며 언어·사회성·인지가 빠르게 발달하는 시기입니다.",
    domains: [
      { id: "lang", name: "언어 발달", type: "d-lang", ref: "CDC Developmental Milestones 2022 · DSM-5-TR (2022)", items: [
        { id: "l1", badge: "4세", text: "네 단어 이상 붙여서 말하지 않는다", sub: '"나 오늘 블록 놀이 했어" 같은 말 없음' },
        { id: "l2", badge: "4세", text: "오늘 있었던 일을 간단하게 말하지 못한다", sub: '"오늘 뭐 했어?" 물으면 단어만 말하거나 대답 못 함' },
        { id: "l3", badge: "5세", text: "자기 이름과 사는 동네를 말하지 못한다" },
        { id: "l4", badge: "공통", text: "혼자 말은 많은데 대화가 이어지지 않는다", sub: "상대방 말은 듣지 않고 자기 말만 계속함" },
        { id: "l5", badge: "공통", text: "가족 외에는 알아듣기 힘들 만큼 발음이 부정확하다" },
      ]},
      { id: "social", name: "사회적 상호작용", type: "d-social", ref: "DSM-5-TR (2022) · M-CHAT-R/F (Robins et al., 2014)", items: [
        { id: "s1", badge: "공통", text: "또래보다 어른하고만 놀려 한다" },
        { id: "s2", badge: "공통", text: "친구가 생기는 것에 관심이 없다" },
        { id: "s3", badge: "공통", text: "놀이 규칙을 이해하지 못하거나 자꾸 어긴다", sub: "보드게임, 술래잡기 등 규칙 있는 놀이 거부" },
        { id: "s4", badge: "공통", text: "화난 얼굴, 슬픈 얼굴을 구별하지 못한다" },
        { id: "s5", badge: "공통", text: "유치원 체육, 율동 등 단체 활동을 극도로 거부한다" },
      ]},
      { id: "behavior", name: "행동 패턴", type: "d-behavior", ref: "DSM-5-TR (2022) 제한적·반복적 행동 기준 (criterion B)", items: [
        { id: "b1", badge: "공통", text: "특정 주제나 장난감 집착이 심해서 다른 활동으로 넘어가지 못한다" },
        { id: "b2", badge: "공통", text: "순서나 루틴이 조금만 바뀌어도 소리 지르거나 바닥에 드러눕는다" },
        { id: "b3", badge: "공통", text: "같은 말이나 행동을 상황과 관계없이 계속 반복한다" },
        { id: "b4", badge: "공통", text: "특정 소리, 옷 감촉, 음식 질감에 또래보다 훨씬 예민하거나 전혀 반응하지 않는다" },
      ]},
      { id: "cognitive", name: "인지 발달", type: "d-cognitive", ref: "CDC Developmental Milestones 2022 · WPPSI-IV", items: [
        { id: "c1", badge: "4세", text: "이야기를 들어도 무슨 일이 먼저 일어났는지 모른다" },
        { id: "c2", badge: "4세", text: '"이거랑 이거 같아, 달라?" 물으면 구별하지 못한다' },
        { id: "c3", badge: "5세", text: "하나부터 열까지 세지 못한다" },
        { id: "c4", badge: "5세", text: "자기 이름을 쓰지 못한다" },
        { id: "c5", badge: "공통", text: "좋아하는 활동도 5~10분 이상 이어가지 못한다" },
      ]},
      { id: "selfregulation", name: "자기조절", type: "d-self", ref: "DSM-5-TR (2022) · Conners Early Childhood", items: [
        { id: "r1", badge: "공통", text: "원하는 게 안 되면 30분 이상 달래도 진정이 안 된다" },
        { id: "r2", badge: "공통", text: "줄을 서거나 차례를 기다리는 걸 또래보다 훨씬 힘들어한다" },
        { id: "r3", badge: "공통", text: "하지 말라고 해도 뛰거나 물건을 던지는 행동을 멈추지 못한다" },
        { id: "r4", badge: "공통", text: "새로운 장소나 사람 앞에서 일상생활이 어려울 만큼 불안해한다", sub: "유치원, 병원, 마트 등" },
      ]}
    ]
  },
  "60-72": {
    label: "만 6–7세", title: "만 6–7세 발달 체크리스트", desc: "초등학교 입학 전후, 학습·또래 관계·자기조절이 본격적으로 중요해지는 시기입니다.",
    domains: [
      { id: "lang", name: "언어 발달", type: "d-lang", ref: "CDC Developmental Milestones 2022 · DSM-5-TR (2022)", items: [
        { id: "l1", badge: "6세", text: "있었던 일을 앞뒤 순서에 맞게 이야기하지 못한다", sub: '"먼저 뭐 했어, 그다음엔?" 물으면 뒤죽박죽' },
        { id: "l2", badge: "6세", text: "모르는 단어가 나와도 물어보지 않고 그냥 넘긴다" },
        { id: "l3", badge: "7세", text: "짧은 이야기를 듣고 무슨 내용인지 말하지 못한다" },
        { id: "l4", badge: "공통", text: "말은 많은데 주제에서 계속 벗어난다" },
        { id: "l5", badge: "공통", text: "상대방 말을 끊고 자기 말만 계속한다" },
      ]},
      { id: "social", name: "사회적 상호작용", type: "d-social", ref: "DSM-5-TR (2022) · BASC-3", items: [
        { id: "s1", badge: "공통", text: "친구가 없거나 늘 혼자 논다" },
        { id: "s2", badge: "공통", text: "친구가 싫어하는 행동을 반복해도 알아채지 못한다" },
        { id: "s3", badge: "공통", text: "농담이나 빈말을 곧이곧대로 받아들인다", sub: '"너 진짜 웃기다"를 욕으로 받아들이는 경우' },
        { id: "s4", badge: "공통", text: "지거나 실수하면 물건을 던지거나 뒤집는 등 또래보다 훨씬 강하게 반응한다" },
        { id: "s5", badge: "공통", text: "쉬는 시간에 뭘 해야 할지 몰라 혼자 서 있는다" },
      ]},
      { id: "behavior", name: "행동 패턴", type: "d-behavior", ref: "DSM-5-TR (2022) 제한적·반복적 행동 기준 (criterion B)", items: [
        { id: "b1", badge: "공통", text: "특정 주제 얘기를 상황과 관계없이 계속 꺼낸다" },
        { id: "b2", badge: "공통", text: "정해진 순서나 자리가 바뀌면 수업 참여가 매우 어려울 만큼 힘들어한다" },
        { id: "b3", badge: "공통", text: "연필 감촉, 교복 소매, 급식 냄새 등에 또래보다 훨씬 예민하게 반응한다" },
        { id: "b4", badge: "공통", text: "손 흔들기, 몸 흔들기 등이 수업 중에도 멈추지 않는다" },
      ]},
      { id: "cognitive", name: "인지 발달", type: "d-cognitive", ref: "CDC Developmental Milestones 2022 · WPPSI-IV · Conners 3", items: [
        { id: "c1", badge: "6세", text: "자기 이름, 전화번호를 쓰거나 말하지 못한다" },
        { id: "c2", badge: "6세", text: "글자를 거울처럼 뒤집어 쓰는 일이 자주 반복된다", sub: "b/d, p/q, ㄱ/ㄴ 방향 혼동이 지속됨" },
        { id: "c3", badge: "7세", text: "두 자리 수 덧셈, 뺄셈을 이해하지 못한다" },
        { id: "c4", badge: "공통", text: "선생님 말을 듣고 따라 하는 것이 또래보다 현저히 느리다" },
        { id: "c5", badge: "공통", text: "숙제나 준비물을 매일 빠뜨린다" },
      ]},
      { id: "selfregulation", name: "자기조절", type: "d-self", ref: "DSM-5-TR (2022) · Conners 3 · BASC-3", items: [
        { id: "r1", badge: "공통", text: "수업 중 자리에 앉아 있지 못하고 돌아다닌다" },
        { id: "r2", badge: "공통", text: "하지 말라는 행동을 반복하면서도 왜 혼나는지 모른다" },
        { id: "r3", badge: "공통", text: "작은 일에도 울거나 소리 지르는 일이 매일 반복된다" },
        { id: "r4", badge: "공통", text: "숙제나 해야 할 일을 시작하는 것 자체를 매일 극도로 거부한다" },
      ]}
    ]
  },
  "school": {
    label: "만 8–9세", title: "만 8–9세 발달 체크리스트", desc: "학교 생활이 복잡해지고, 또래 관계·학습·자기조절 어려움이 본격적으로 드러나는 시기입니다.",
    domains: [
      { id: "lang", name: "언어 발달", type: "d-lang", ref: "DSM-5-TR (2022)", items: [
        { id: "l1", badge: "공통", text: "자기 생각을 말로 설명하는 것을 매우 어려워한다", sub: '"왜 그렇게 생각해?" 물으면 "그냥요"로 끝남' },
        { id: "l2", badge: "공통", text: "책을 읽어도 무슨 내용인지 말하지 못한다" },
        { id: "l3", badge: "공통", text: "대화할 때 눈을 거의 마주치지 않는다" },
        { id: "l4", badge: "공통", text: "비유나 속담을 문자 그대로 받아들인다", sub: '"발이 넓다"를 신발 사이즈로 받아들임' },
      ]},
      { id: "social", name: "사회적 상호작용", type: "d-social", ref: "DSM-5-TR (2022) · BASC-3", items: [
        { id: "s1", badge: "공통", text: "친구 관계가 늘 오래가지 못하고 끊어진다" },
        { id: "s2", badge: "공통", text: "그룹 과제에서 혼자 튀는 행동으로 친구들과 갈등이 생긴다" },
        { id: "s3", badge: "공통", text: "상대방이 화났는지 기쁜지 표정으로 읽지 못한다" },
        { id: "s4", badge: "공통", text: "친구와 노는 것보다 혼자 유튜브, 게임을 압도적으로 선호한다" },
        { id: "s5", badge: "공통", text: "선생님이나 어른에게 지나치게 의존하거나 반대로 완전히 무시한다" },
      ]},
      { id: "behavior", name: "행동 패턴", type: "d-behavior", ref: "DSM-5-TR (2022) 제한적·반복적 행동 기준 (criterion B)", items: [
        { id: "b1", badge: "공통", text: "특정 관심사 얘기를 상대가 싫어해도 멈추지 않는다" },
        { id: "b2", badge: "공통", text: "갑작스러운 일정 변경에 하루 전체가 힘들어진다" },
        { id: "b3", badge: "공통", text: "특정 음식, 소리, 냄새에 대한 예민함이 학교생활을 방해한다" },
        { id: "b4", badge: "공통", text: "스트레스 상황에서 특정 행동이나 말을 반복하는 일이 심해진다" },
      ]},
      { id: "cognitive", name: "인지 발달", type: "d-cognitive", ref: "DSM-5-TR (2022) · Conners 3 · K-ABC-II", items: [
        { id: "c1", badge: "공통", text: "읽기는 되는데 내용 이해가 또래보다 현저히 떨어진다" },
        { id: "c2", badge: "공통", text: "수식은 아는데 문장으로 된 수학 문제가 전혀 안 된다", sub: '"사과 3개에서 1개를 먹으면?" 은 알아도 문장으로 나오면 모름' },
        { id: "c3", badge: "공통", text: '"30분 후에 출발해" 같은 시간 개념이 전혀 감이 없다' },
        { id: "c4", badge: "공통", text: "숙제를 어디서부터 시작해야 할지 몰라 매일 멈춰있다" },
      ]},
      { id: "selfregulation", name: "자기조절", type: "d-self", ref: "DSM-5-TR (2022) · Conners 3 · BASC-3", items: [
        { id: "r1", badge: "공통", text: "감정이 폭발하면 주변 물건이나 사람을 밀거나 치는 행동이 나온다" },
        { id: "r2", badge: "공통", text: "숙제나 과제를 시작하기까지 매일 1시간 이상 걸린다" },
        { id: "r3", badge: "공통", text: "실수나 실패를 두려워해서 새로운 시도 자체를 안 한다" },
        { id: "r4", badge: "공통", text: "학교 가기 싫다는 말을 거의 매일 하거나 두통, 복통을 자주 호소한다" },
      ]}
    ]
  }
};

let currentAge = "18-36";
let answers = {};

function buildSections() {
  const wrap = document.getElementById('checklistWrap');
  wrap.innerHTML = '';

  Object.entries(DATA).forEach(([ageKey, ageData]) => {
    const section = document.createElement('div');
    section.className = 'age-section' + (ageKey === '18-36' ? ' active' : '');
    section.id = 'section-' + ageKey;

    let html = `<div class="age-header"><div class="age-header-badge">${ageData.label}</div><div class="age-header-title">${ageData.title}</div><div class="age-header-desc">${ageData.desc}</div></div>`;

    ageData.domains.forEach(domain => {
      html += `<div class="domain-block"><div class="domain-label ${domain.type}"><span class="domain-dot"></span>${domain.name}</div>`;
      if (domain.ref) html += `<div class="domain-ref">${domain.ref}</div>`;

      domain.items.forEach(item => {
        const badges = [];
        if (item.badge) {
          const bc = item.badge === '공통' ? 'badge-common' : 'badge-month';
          badges.push(`<span class="item-badge ${bc}">${item.badge}</span>`);
        }
        if (item.alert) badges.push(`<span class="item-badge badge-alert">적색신호</span>`);

        html += `<div class="check-item" id="item-${item.id}-${ageKey}">
          <div class="item-top">
            ${badges.length ? `<div class="item-badges">${badges.join('')}</div>` : ''}
            <div class="item-text">${item.text}</div>
          </div>
          ${item.sub ? `<div class="item-sub">${item.sub}</div>` : ''}
          <div class="item-actions">
            <button class="yn-btn yes-btn" onclick="setAnswer('${item.id}','${ageKey}','${domain.id}','yes')">✓ 예, 해당돼요</button>
            <button class="yn-btn no-btn" onclick="setAnswer('${item.id}','${ageKey}','${domain.id}','no')">✕ 해당 없어요</button>
          </div>
        </div>`;
      });

      html += `</div>`;
    });

    section.innerHTML = html;
    wrap.appendChild(section);
  });
}

function setAnswer(itemId, ageKey, domainId, val) {
  const key = `${ageKey}__${domainId}__${itemId}`;
  answers[key] = val;

  const itemEl = document.getElementById(`item-${itemId}-${ageKey}`);
  itemEl.classList.remove('answered-yes', 'answered-no');
  itemEl.classList.add(val === 'yes' ? 'answered-yes' : 'answered-no');

  const btns = itemEl.querySelectorAll('.yn-btn');
  btns[0].classList.toggle('selected-yes', val === 'yes');
  btns[0].classList.toggle('selected-no', false);
  btns[1].classList.toggle('selected-no', val === 'no');
  btns[1].classList.toggle('selected-yes', false);

  updatePanel();
}

function getAgeAnswers() {
  const prefix = currentAge + '__';
  return {
    yes: Object.entries(answers).filter(([k,v]) => k.startsWith(prefix) && v === 'yes').length,
    total: Object.entries(answers).filter(([k,v]) => k.startsWith(prefix)).length
  };
}

function updatePanel() {
  const { yes, total } = getAgeAnswers();
  document.getElementById('yesCount').textContent = yes;
  document.getElementById('totalCount').textContent = total;

  const allItems = DATA[currentAge].domains.reduce((a,d) => a + d.items.length, 0);
  const pct = allItems > 0 ? Math.round((total / allItems) * 100) : 0;

  document.getElementById('barFill').style.width = pct + '%';
  document.getElementById('barLabel').textContent =
    total === 0 ? '항목에 응답해 주세요' :
    pct < 100 ? `${total}/${allItems} 응답 완료` :
    '모든 항목 응답 완료 ✓';
}

function showResult() {
  const ageData = DATA[currentAge];
  const prefix = currentAge + '__';
  const domainYes = {}, domainTotal = {};

  ageData.domains.forEach(d => {
    domainYes[d.id] = 0;
    domainTotal[d.id] = d.items.length;
  });

  Object.entries(answers).forEach(([k, v]) => {
    if (!k.startsWith(prefix)) return;
    const dId = k.split('__')[1];
    if (v === 'yes' && domainYes[dId] !== undefined) domainYes[dId]++;
  });

  const totalYes = Object.values(domainYes).reduce((a,b) => a+b, 0);
  const totalItems = ageData.domains.reduce((a,d) => a + d.items.length, 0);
  const pct = totalItems > 0 ? Math.round((totalYes / totalItems) * 100) : 0;

  document.getElementById('ringNum').textContent = totalYes;
  setTimeout(() => {
    document.getElementById('ringFill').style.strokeDashoffset = 201 - (201 * pct / 100);
  }, 100);

  document.getElementById('modalTitle').textContent = `${ageData.label} 체크리스트 결과`;
  document.getElementById('modalSubtitle').textContent = `총 ${totalItems}개 항목 중 ${totalYes}개 해당`;

  const langAlertItems = [];
  ageData.domains.forEach(d => {
    d.items.forEach(item => {
      if (item.alert && answers[`${currentAge}__${d.id}__${item.id}`] === 'yes') {
        langAlertItems.push(item.id);
      }
    });
  });

  const hasLangAlert = langAlertItems.length > 0;
  const hasDomainTwo = Object.values(domainYes).some(v => v >= 2);

  /* 핵심 수정: 전체합 2개 기준 삭제 */
  const needsConsult = hasLangAlert || hasDomainTwo;

  let scoreTitle, scoreDesc, adviceText;

  if (totalYes === 0) {
    scoreTitle = '현재 걱정되는 항목이 없네요 😊';
    scoreDesc = '현재 선별 항목에는 해당되지 않습니다. 발달은 개인차가 있으니 지속적인 관찰을 이어가세요.';
    adviceText = '체크리스트에 해당 없어도 "뭔가 다른 것 같다"는 느낌이 드신다면 상담을 요청하셔도 됩니다. 부모님의 직관은 중요한 정보입니다.';
  } else if (!needsConsult) {
    scoreTitle = '일부 항목이 해당됩니다';
    scoreDesc = '해당 항목이 있지만 한 영역에서 2개 미만입니다. 지속적으로 관찰하고, 걱정이 되신다면 전문가와 이야기해보세요.';
    adviceText = '"이 정도면 괜찮겠지" 하고 넘기지 마세요. 조기 발견과 조기 개입이 가장 효과적입니다.';
  } else {
    scoreTitle = hasLangAlert
      ? '지금 바로 전문가 상담을 받아보세요'
      : '전문가 상담을 권장합니다';
    scoreDesc = hasLangAlert
      ? '언어 퇴행 항목이 해당됩니다. 1개라도 해당되면 즉시 전문가와 확인이 필요합니다.'
      : '한 영역에서 2개 이상 해당됩니다. 빠른 전문가 상담을 권장합니다.';
    adviceText = '체크리스트는 선별 도구이며 진단을 의미하지 않습니다. 하지만 조기에 전문가와 이야기하는 것이 아이에게 가장 도움이 됩니다.';
  }

  document.getElementById('scoreTitle').textContent = scoreTitle;
  document.getElementById('scoreDesc').textContent = scoreDesc;
  document.getElementById('adviceText').textContent = adviceText;

  const consultBox = document.getElementById('consultBox');
  const consultUrgent = document.getElementById('consultUrgent');

  /* 핵심 수정: 상담권장일 때만 박스 노출 */
  consultBox.style.display = needsConsult ? 'block' : 'none';
  consultUrgent.style.display = hasLangAlert ? 'flex' : 'none';

  const colorMap = {
    lang: '#D97B8E',
    social: '#E8B84B',
    behavior: '#8B7AB8',
    cognitive: '#3A7A50',
    motor: '#2A6A9A',
    selfregulation: '#B85A30'
  };

  document.getElementById('domainResults').innerHTML = ageData.domains.map(d => {
    const yes = domainYes[d.id];
    const tot = domainTotal[d.id];
    const p = Math.round((yes / tot) * 100);
    const color = colorMap[d.id] || '#D97B8E';

    return `
      <div class="domain-result-item">
        <div class="domain-result-name">${d.name}</div>
        <div class="domain-mini-bar">
          <div class="domain-mini-fill" style="width:0%;background:${color}" data-pct="${p}"></div>
        </div>
        <div class="domain-result-count">${yes}/${tot}</div>
      </div>
    `;
  }).join('');

  document.getElementById('modalOverlay').classList.add('open');

  setTimeout(() => {
    document.querySelectorAll('.domain-mini-fill').forEach(el => {
      el.style.width = el.dataset.pct + '%';
    });
  }, 200);
}

function resetAnswers() {
  const prefix = currentAge + '__';
  Object.keys(answers).forEach(k => {
    if (k.startsWith(prefix)) delete answers[k];
  });

  document.querySelectorAll('#section-' + currentAge + ' .check-item').forEach(el => el.classList.remove('answered-yes', 'answered-no'));
  document.querySelectorAll('#section-' + currentAge + ' .yn-btn').forEach(btn => btn.classList.remove('selected-yes', 'selected-no'));

  updatePanel();
  document.getElementById('modalOverlay').classList.remove('open');
}

document.querySelectorAll('.age-tab').forEach(tab => {
  tab.addEventListener('click', () => {
    currentAge = tab.dataset.age;
    document.querySelectorAll('.age-tab').forEach(t => t.classList.remove('active'));
    tab.classList.add('active');
    document.querySelectorAll('.age-section').forEach(s => s.classList.remove('active'));
    document.getElementById('section-' + currentAge).classList.add('active');
    updatePanel();
  });
});

document.getElementById('showResultBtn').addEventListener('click', showResult);
document.getElementById('modalClose').addEventListener('click', () => document.getElementById('modalOverlay').classList.remove('open'));
document.getElementById('resetBtn').addEventListener('click', resetAnswers);
document.getElementById('modalOverlay').addEventListener('click', e => {
  if (e.target === document.getElementById('modalOverlay')) {
    document.getElementById('modalOverlay').classList.remove('open');
  }
});

buildSections();
updatePanel();
</script>
</body>
</html>
