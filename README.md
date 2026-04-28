# ISCE-2026-GUIA-PARCIAL



<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ICSE 2026 — Guía Primer Parcial</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@400;600&family=IBM+Plex+Sans:ital,wght@0,400;0,500;0,600;0,700;1,400&display=swap');

  :root {
    --bg: #0f0f0f;
    --bg2: #181818;
    --bg3: #212121;
    --bg4: #2a2a2a;
    --border: #333;
    --border2: #444;
    --text: #e8e6e1;
    --text2: #a09e99;
    --text3: #6b6966;
    --blue: #4a9eff;
    --blue-bg: #0d2140;
    --blue-dim: #1a3a6b;
    --teal: #3fcf8e;
    --teal-bg: #062918;
    --amber: #f0a030;
    --amber-bg: #2a1a00;
    --red: #f06060;
    --red-bg: #2a0a0a;
    --purple: #a088f0;
    --purple-bg: #1a0f38;
    --coral: #f07060;
    --coral-bg: #2a0d08;
    --green: #60c060;
    --green-bg: #0a1f0a;
    --gold: #e8c060;
    --gold-bg: #231900;
  }
  * { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-behavior: smooth; }
  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'IBM Plex Sans', -apple-system, sans-serif;
    font-size: 15px;
    line-height: 1.7;
    max-width: 860px;
    margin: 0 auto;
    padding: 2rem 1.5rem 4rem;
  }

  .site-header {
    border-bottom: 1px solid var(--border);
    padding-bottom: 1.5rem;
    margin-bottom: 2rem;
  }
  .site-header h1 { font-size: 26px; font-weight: 700; color: var(--text); margin-bottom: 6px; }
  .site-header p { color: var(--text2); font-size: 14px; }
  .badges { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 12px; }
  .badge { font-size: 12px; font-weight: 600; padding: 4px 12px; border-radius: 99px; letter-spacing: 0.03em; }
  .badge-parcial { background: var(--red-bg); color: var(--red); border: 1px solid #4a1010; }
  .badge-fecha { background: var(--amber-bg); color: var(--amber); border: 1px solid #4a2a00; }
  .badge-temas { background: var(--blue-bg); color: var(--blue); border: 1px solid var(--blue-dim); }

  .alert { background: var(--gold-bg); border: 1px solid #5a4a00; border-left: 4px solid var(--gold); border-radius: 8px; padding: 1rem 1.25rem; margin-bottom: 2rem; font-size: 13.5px; }
  .alert-title { color: var(--gold); font-weight: 600; font-size: 14px; margin-bottom: 6px; }
  .alert p { color: #c8aa50; line-height: 1.6; }
  .alert strong { color: var(--gold); }

  nav {
    position: sticky; top: 0;
    background: var(--bg);
    border-bottom: 1px solid var(--border);
    padding: 10px 0; margin-bottom: 2rem; z-index: 100;
    display: flex; gap: 6px; flex-wrap: wrap;
  }
  nav a { color: var(--text2); text-decoration: none; font-size: 12.5px; font-weight: 500; padding: 5px 11px; border-radius: 6px; border: 1px solid transparent; transition: all 0.15s; white-space: nowrap; }
  nav a:hover { background: var(--bg3); color: var(--text); border-color: var(--border); }

  .section { margin-bottom: 3.5rem; padding-top: 0.5rem; }
  .section-header { display: flex; align-items: center; gap: 12px; margin-bottom: 1.5rem; padding-bottom: 0.75rem; border-bottom: 1px solid var(--border); }
  .section-num { width: 32px; height: 32px; border-radius: 8px; display: flex; align-items: center; justify-content: center; font-size: 14px; font-weight: 700; flex-shrink: 0; }
  .section-header h2 { font-size: 20px; font-weight: 600; color: var(--text); }
  .section-header p { font-size: 13px; color: var(--text2); margin-top: 2px; }

  .subsection { margin-bottom: 1.75rem; }
  .subsection-title { font-size: 13px; font-weight: 600; text-transform: uppercase; letter-spacing: 0.08em; color: var(--text3); margin-bottom: 0.75rem; padding-left: 10px; border-left: 2px solid var(--border2); }

  .cards { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 10px; margin-bottom: 1rem; }
  .card { background: var(--bg2); border: 1px solid var(--border); border-radius: 10px; padding: 1rem 1.1rem; }
  .card-label { font-size: 11px; font-weight: 600; text-transform: uppercase; letter-spacing: 0.06em; margin-bottom: 5px; }
  .card-title { font-size: 14px; font-weight: 600; color: var(--text); margin-bottom: 4px; }
  .card-body { font-size: 13px; color: var(--text2); line-height: 1.65; }

  .keybox { background: var(--bg3); border: 1px solid var(--border); border-left: 3px solid var(--border2); border-radius: 8px; padding: 0.8rem 1rem; font-size: 13.5px; color: var(--text2); line-height: 1.7; margin: 0.6rem 0; }
  .keybox strong { color: var(--text); }
  .keybox.blue { border-left-color: var(--blue); background: var(--blue-bg); color: #8fc8ff; }
  .keybox.blue strong { color: var(--blue); }
  .keybox.teal { border-left-color: var(--teal); background: var(--teal-bg); color: #7ae0b4; }
  .keybox.teal strong { color: var(--teal); }
  .keybox.amber { border-left-color: var(--amber); background: var(--amber-bg); color: #c8882a; }
  .keybox.amber strong { color: var(--amber); }
  .keybox.red { border-left-color: var(--red); background: var(--red-bg); color: #e89090; }
  .keybox.red strong { color: var(--red); }
  .keybox.purple { border-left-color: var(--purple); background: var(--purple-bg); color: #c0aaf8; }
  .keybox.purple strong { color: var(--purple); }
  .keybox.gold { border-left-color: var(--gold); background: var(--gold-bg); color: #c8aa50; }
  .keybox.gold strong { color: var(--gold); }

  .exam-tip { background: var(--gold-bg); border: 1px solid #4a3800; border-left: 3px solid var(--gold); border-radius: 8px; padding: 0.7rem 1rem; font-size: 13px; color: #b89840; margin: 0.5rem 0; }
  .exam-tip::before { content: "★ Tip de examen: "; color: var(--gold); font-weight: 600; }

  .table-wrap { border: 1px solid var(--border); border-radius: 10px; overflow: hidden; margin: 0.75rem 0 1.25rem; overflow-x: auto; }
  table { width: 100%; border-collapse: collapse; font-size: 13px; min-width: 500px; }
  thead tr { background: var(--bg3); }
  th { text-align: left; padding: 10px 14px; color: var(--text2); font-weight: 600; font-size: 12px; text-transform: uppercase; letter-spacing: 0.05em; border-bottom: 1px solid var(--border); }
  td { padding: 9px 14px; color: var(--text2); border-bottom: 1px solid var(--border); vertical-align: top; line-height: 1.55; }
  td:first-child { color: var(--text3); font-size: 12px; font-weight: 600; background: var(--bg3); white-space: nowrap; }
  tr:last-child td { border-bottom: none; }
  tr:hover td { background: var(--bg2); }
  tr:hover td:first-child { background: var(--bg3); }

  .timeline { margin: 0.75rem 0 1.25rem; }
  .tl-item { display: flex; gap: 14px; margin-bottom: 1.1rem; }
  .tl-left { display: flex; flex-direction: column; align-items: center; flex-shrink: 0; width: 14px; }
  .tl-dot { width: 12px; height: 12px; border-radius: 50%; flex-shrink: 0; margin-top: 4px; }
  .tl-line-seg { flex: 1; width: 1px; background: var(--border); margin-top: 4px; min-height: 16px; }
  .tl-content { flex: 1; padding-bottom: 0.4rem; }
  .tl-year { font-size: 11px; font-weight: 700; letter-spacing: 0.06em; margin-bottom: 2px; }
  .tl-title { font-size: 13.5px; font-weight: 600; color: var(--text); margin-bottom: 2px; }
  .tl-text { font-size: 13px; color: var(--text2); line-height: 1.6; }

  .pills { display: flex; flex-wrap: wrap; gap: 6px; margin: 0.6rem 0; }
  .pill { font-size: 12.5px; font-weight: 500; padding: 4px 12px; border-radius: 99px; border: 1px solid; }
  .pill-blue { background: var(--blue-bg); color: #7abfff; border-color: var(--blue-dim); }
  .pill-teal { background: var(--teal-bg); color: #5ecf9e; border-color: #0a3d20; }
  .pill-amber { background: var(--amber-bg); color: #d08828; border-color: #3a2200; }
  .pill-red { background: var(--red-bg); color: #e08080; border-color: #3a1010; }
  .pill-purple { background: var(--purple-bg); color: #b0a0f8; border-color: #2a1a50; }

  .accordion { margin: 0.5rem 0 1.25rem; }
  .acc-item { background: var(--bg2); border: 1px solid var(--border); border-radius: 8px; margin-bottom: 6px; overflow: hidden; }
  .acc-q { padding: 0.8rem 1rem; font-size: 13.5px; font-weight: 500; color: var(--text); cursor: pointer; display: flex; justify-content: space-between; align-items: flex-start; gap: 10px; user-select: none; }
  .acc-q:hover { background: var(--bg3); }
  .acc-icon { width: 18px; height: 18px; border-radius: 50%; background: var(--bg4); display: flex; align-items: center; justify-content: center; font-size: 11px; color: var(--text3); flex-shrink: 0; transition: transform 0.2s; margin-top: 2px; }
  .acc-a { max-height: 0; overflow: hidden; transition: max-height 0.3s ease; }
  .acc-a-inner { padding: 0 1rem 0.9rem; font-size: 13px; color: var(--text2); line-height: 1.7; border-top: 1px solid var(--border); padding-top: 0.8rem; }
  .acc-a-inner strong { color: var(--text); }
  .acc-item.open .acc-icon { transform: rotate(45deg); }
  .acc-item.open .acc-a { max-height: 600px; }

  .triangle-section { background: linear-gradient(135deg, #1a1200 0%, #0f0e00 100%); border: 1px solid #5a4800; border-radius: 12px; padding: 1.5rem; margin-bottom: 2rem; }
  .triangle-title { color: var(--gold); font-size: 16px; font-weight: 700; margin-bottom: 4px; display: flex; align-items: center; gap: 8px; }
  .triangle-subtitle { color: #8a7a30; font-size: 13px; margin-bottom: 1.25rem; }
  .triangle-cards { display: grid; grid-template-columns: repeat(auto-fit, minmax(230px, 1fr)); gap: 10px; }
  .tri-card { background: rgba(255,255,255,0.03); border: 1px solid #3a3000; border-radius: 8px; padding: 1rem; }
  .tri-card-title { color: var(--gold); font-size: 14px; font-weight: 600; margin-bottom: 4px; }
  .tri-card-sub { color: #8a7a30; font-size: 11px; font-weight: 600; text-transform: uppercase; letter-spacing: 0.05em; margin-bottom: 6px; }
  .tri-card p { color: #a09030; font-size: 13px; line-height: 1.6; }
  .tri-card strong { color: #d4a830; }

  .traps-section { background: var(--red-bg); border: 1px solid #3a1010; border-radius: 12px; padding: 1.5rem; margin-bottom: 2rem; }
  .traps-title { color: var(--red); font-size: 15px; font-weight: 700; margin-bottom: 1rem; }
  .trap-item { display: flex; gap: 10px; margin-bottom: 0.75rem; }
  .trap-dot { width: 6px; height: 6px; border-radius: 50%; background: var(--red); flex-shrink: 0; margin-top: 8px; }
  .trap-text { font-size: 13px; color: #e08080; line-height: 1.6; }
  .trap-text strong { color: var(--red); }

  hr { border: none; border-top: 1px solid var(--border); margin: 2rem 0; }
  footer { margin-top: 3rem; padding-top: 1.5rem; border-top: 1px solid var(--border); text-align: center; font-size: 12px; color: var(--text3); }

  /* ========== QUIZ SYSTEM ========== */
  .quiz-launcher {
    margin: 1.5rem 0 0.5rem;
    display: flex;
    align-items: center;
    gap: 12px;
    flex-wrap: wrap;
  }
  .quiz-btn {
    background: linear-gradient(135deg, #0d3a6b, #1a5090);
    border: 1px solid var(--blue);
    color: var(--blue);
    font-family: 'IBM Plex Mono', monospace;
    font-size: 12px;
    font-weight: 600;
    padding: 8px 18px;
    border-radius: 8px;
    cursor: pointer;
    letter-spacing: 0.05em;
    transition: all 0.15s;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .quiz-btn:hover { background: linear-gradient(135deg, #1a5090, #2060b0); transform: translateY(-1px); }
  .quiz-btn:active { transform: translateY(0); }
  .quiz-btn .btn-icon { font-size: 14px; }

  .quiz-stats-mini {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 11px;
    color: var(--text3);
    display: flex;
    gap: 12px;
    flex-wrap: wrap;
  }
  .stat-correct { color: var(--teal); }
  .stat-wrong { color: var(--red); }

  /* QUIZ OVERLAY */
  .quiz-overlay {
    display: none;
    position: fixed;
    inset: 0;
    background: rgba(0,0,0,0.95);
    z-index: 1000;
    overflow-y: auto;
    padding: 2rem 1rem;
  }
  .quiz-overlay.active { display: flex; flex-direction: column; align-items: center; justify-content: flex-start; }

  .quiz-container {
    width: 100%;
    max-width: 680px;
    margin: 0 auto;
  }

  .quiz-topbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 1.5rem;
    padding-bottom: 1rem;
    border-bottom: 1px solid var(--border);
  }
  .quiz-module-name {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 12px;
    color: var(--text2);
    font-weight: 600;
    letter-spacing: 0.06em;
  }
  .quiz-progress-wrap { display: flex; align-items: center; gap: 10px; }
  .quiz-progress-bar-outer {
    width: 120px; height: 4px;
    background: var(--bg3);
    border-radius: 2px;
    overflow: hidden;
  }
  .quiz-progress-bar-inner {
    height: 100%;
    background: var(--blue);
    border-radius: 2px;
    transition: width 0.3s;
  }
  .quiz-progress-text { font-family: 'IBM Plex Mono', monospace; font-size: 11px; color: var(--text3); }
  .quiz-close-btn {
    background: var(--bg3);
    border: 1px solid var(--border);
    color: var(--text2);
    font-size: 12px;
    font-weight: 600;
    padding: 5px 12px;
    border-radius: 6px;
    cursor: pointer;
    transition: all 0.15s;
  }
  .quiz-close-btn:hover { background: var(--red-bg); border-color: var(--red); color: var(--red); }

  /* Streak + score bar */
  .quiz-scorebar {
    display: flex;
    gap: 14px;
    margin-bottom: 1.5rem;
    flex-wrap: wrap;
  }
  .score-chip {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 12px;
    padding: 5px 12px;
    border-radius: 6px;
    font-weight: 600;
    border: 1px solid;
  }
  .score-chip.correct { background: var(--teal-bg); color: var(--teal); border-color: #0a3d20; }
  .score-chip.wrong { background: var(--red-bg); color: var(--red); border-color: #3a1010; }
  .score-chip.streak { background: var(--amber-bg); color: var(--amber); border-color: #4a2a00; }
  .score-chip.total { background: var(--bg3); color: var(--text2); border-color: var(--border); }

  /* Question card */
  .quiz-card {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 14px;
    padding: 1.75rem;
    margin-bottom: 1.25rem;
    animation: slideIn 0.25s ease;
  }
  @keyframes slideIn { from { opacity: 0; transform: translateY(12px); } to { opacity: 1; transform: translateY(0); } }

  .quiz-badge-row { display: flex; gap: 8px; margin-bottom: 1rem; flex-wrap: wrap; align-items: center; }
  .q-badge { font-family: 'IBM Plex Mono', monospace; font-size: 10px; font-weight: 700; padding: 3px 8px; border-radius: 4px; letter-spacing: 0.05em; }
  .q-badge.review { background: var(--amber-bg); color: var(--amber); border: 1px solid #4a2a00; }
  .q-badge.new { background: var(--blue-bg); color: var(--blue); border: 1px solid var(--blue-dim); }
  .q-badge.difficulty { background: var(--bg3); color: var(--text3); border: 1px solid var(--border); }

  .quiz-question {
    font-size: 16px;
    font-weight: 600;
    color: var(--text);
    line-height: 1.5;
    margin-bottom: 1.5rem;
  }

  .quiz-options { display: flex; flex-direction: column; gap: 8px; }
  .quiz-option {
    background: var(--bg3);
    border: 1.5px solid var(--border);
    border-radius: 10px;
    padding: 0.85rem 1.1rem;
    font-size: 14px;
    color: var(--text2);
    cursor: pointer;
    transition: all 0.15s;
    display: flex;
    align-items: flex-start;
    gap: 10px;
    text-align: left;
    line-height: 1.5;
  }
  .quiz-option:hover:not(.disabled) { background: var(--bg4); border-color: var(--blue); color: var(--text); }
  .quiz-option .opt-letter { font-family: 'IBM Plex Mono', monospace; font-size: 11px; font-weight: 700; color: var(--text3); flex-shrink: 0; margin-top: 2px; min-width: 18px; }
  .quiz-option.correct-pick { background: var(--teal-bg); border-color: var(--teal); color: #7ae0b4; }
  .quiz-option.correct-pick .opt-letter { color: var(--teal); }
  .quiz-option.wrong-pick { background: var(--red-bg); border-color: var(--red); color: #e89090; }
  .quiz-option.wrong-pick .opt-letter { color: var(--red); }
  .quiz-option.correct-answer { background: var(--teal-bg); border-color: var(--teal); color: #7ae0b4; opacity: 0.75; }
  .quiz-option.correct-answer .opt-letter { color: var(--teal); }
  .quiz-option.disabled { cursor: default; }

  /* Feedback */
  .quiz-feedback {
    display: none;
    margin-top: 1rem;
    padding: 1rem 1.1rem;
    border-radius: 10px;
    font-size: 13.5px;
    line-height: 1.65;
    animation: fadeIn 0.2s ease;
  }
  @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
  .quiz-feedback.correct { background: var(--teal-bg); border: 1px solid #0a3d20; color: #7ae0b4; }
  .quiz-feedback.wrong { background: var(--red-bg); border: 1px solid #3a1010; color: #e89090; }
  .quiz-feedback .fb-label { font-weight: 700; margin-bottom: 4px; display: block; }
  .quiz-feedback .fb-explanation { font-size: 13px; }
  .quiz-feedback strong { color: inherit; filter: brightness(1.2); }

  /* Timer / review countdown */
  .review-countdown {
    display: none;
    background: var(--amber-bg);
    border: 1px solid #4a2a00;
    border-radius: 8px;
    padding: 0.6rem 1rem;
    margin-top: 0.75rem;
    font-family: 'IBM Plex Mono', monospace;
    font-size: 12px;
    color: var(--amber);
    display: none;
    align-items: center;
    gap: 10px;
  }
  .review-countdown.visible { display: flex; }
  .countdown-bar-outer { flex: 1; height: 4px; background: var(--bg3); border-radius: 2px; overflow: hidden; }
  .countdown-bar-inner { height: 100%; background: var(--amber); border-radius: 2px; transition: width 0.1s linear; }

  /* Next button */
  .quiz-next-btn {
    display: none;
    margin-top: 1.25rem;
    width: 100%;
    background: linear-gradient(135deg, #0d3a6b, #1a5090);
    border: 1px solid var(--blue);
    color: var(--blue);
    font-family: 'IBM Plex Mono', monospace;
    font-size: 13px;
    font-weight: 600;
    padding: 12px;
    border-radius: 10px;
    cursor: pointer;
    letter-spacing: 0.03em;
    transition: all 0.15s;
  }
  .quiz-next-btn:hover { background: linear-gradient(135deg, #1a5090, #2060b0); }
  .quiz-next-btn.visible { display: block; animation: fadeIn 0.2s ease; }

  /* RESULTS SCREEN */
  .quiz-results {
    display: none;
    flex-direction: column;
    gap: 1.5rem;
    animation: slideIn 0.3s ease;
  }
  .quiz-results.active { display: flex; }

  .results-header { text-align: center; padding: 1.5rem; }
  .results-grade {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 52px;
    font-weight: 700;
    line-height: 1;
    margin-bottom: 8px;
  }
  .results-subtitle { font-size: 14px; color: var(--text2); }

  .results-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
    gap: 10px;
  }
  .res-chip {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 1rem;
    text-align: center;
  }
  .res-chip-val { font-family: 'IBM Plex Mono', monospace; font-size: 24px; font-weight: 700; margin-bottom: 4px; }
  .res-chip-label { font-size: 11px; color: var(--text3); font-weight: 600; text-transform: uppercase; letter-spacing: 0.05em; }
  .res-chip.c { border-color: #0a3d20; }
  .res-chip.c .res-chip-val { color: var(--teal); }
  .res-chip.w { border-color: #3a1010; }
  .res-chip.w .res-chip-val { color: var(--red); }
  .res-chip.s { border-color: #4a2a00; }
  .res-chip.s .res-chip-val { color: var(--amber); }

  /* Results list */
  .results-section-title {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 11px;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    color: var(--text3);
    padding: 0.5rem 0;
    border-bottom: 1px solid var(--border);
    margin-bottom: 0.75rem;
  }
  .results-q-item {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 0.85rem 1rem;
    margin-bottom: 6px;
    font-size: 13px;
  }
  .results-q-item .rq-q { color: var(--text); font-weight: 500; margin-bottom: 4px; }
  .results-q-item .rq-meta { font-family: 'IBM Plex Mono', monospace; font-size: 11px; color: var(--text3); display: flex; gap: 10px; flex-wrap: wrap; }
  .results-q-item.correct { border-left: 3px solid var(--teal); }
  .results-q-item.wrong { border-left: 3px solid var(--red); }
  .rq-times { color: var(--red); }
  .rq-next { color: var(--amber); }
  .rq-ok { color: var(--teal); }

  /* Suggestion box */
  .results-suggestion {
    background: linear-gradient(135deg, #1a1200, #0f0e00);
    border: 1px solid #5a4800;
    border-radius: 12px;
    padding: 1.25rem;
  }
  .sug-title { color: var(--gold); font-size: 14px; font-weight: 700; margin-bottom: 0.75rem; }
  .sug-item { font-size: 13px; color: #a09030; line-height: 1.6; margin-bottom: 4px; }
  .sug-item strong { color: var(--gold); }

  .results-restart-btn {
    background: linear-gradient(135deg, #0d3a6b, #1a5090);
    border: 1px solid var(--blue);
    color: var(--blue);
    font-family: 'IBM Plex Mono', monospace;
    font-size: 13px;
    font-weight: 600;
    padding: 12px;
    border-radius: 10px;
    cursor: pointer;
    letter-spacing: 0.03em;
    transition: all 0.15s;
    width: 100%;
    margin-top: 0.5rem;
  }
  .results-restart-btn:hover { background: linear-gradient(135deg, #1a5090, #2060b0); }

  ::-webkit-scrollbar { width: 6px; height: 6px; }
  ::-webkit-scrollbar-track { background: var(--bg); }
  ::-webkit-scrollbar-thumb { background: var(--border2); border-radius: 3px; }

  @media print { nav { display: none; } body { padding: 1rem; } .acc-a { max-height: none !important; } .quiz-launcher { display: none; } }
</style>
</head>
<body>

<header class="site-header">
  <h1>ICSE 2026 — Guía Primer Parcial</h1>
  <p>Semanas 1 a 5 · Conceptos clave, cuadros comparativos, cronología y cuestionarios interactivos con repaso espaciado</p>
  <div class="badges">
    <span class="badge badge-parcial">Parcial 08/05/2026</span>
    <span class="badge badge-fecha">Semanas 1–5</span>
    <span class="badge badge-temas">7 módulos + quiz por módulo</span>
  </div>
</header>

<div class="triangle-section">
  <div class="triangle-title">★ Triángulo de Oro — Lo que entra en todos los exámenes</div>
  <div class="triangle-subtitle">Tres autores que aparecen en casi todos los modelos. Si los dominás, tenés gran parte resuelta.</div>
  <div class="triangle-cards">
    <div class="tri-card">
      <div class="tri-card-sub">Autor 1</div>
      <div class="tri-card-title">Max Weber — El Estado</div>
      <p>Monopolio de la violencia legítima + las 3 legitimidades. <strong>Tip:</strong> también preguntan qué pasa si el Estado pierde ese monopolio → "Estado fallido".</p>
    </div>
    <div class="tri-card">
      <div class="tri-card-sub">Autor 2</div>
      <div class="tri-card-title">Robert Dahl — Poliarquía</div>
      <p>Tema estrella. Te dan una situación y preguntan qué requisito falta. <strong>Sabé los 6 de memoria.</strong> Definición mínima y procedimental de democracia.</p>
    </div>
    <div class="tri-card">
      <div class="tri-card-sub">Autor 3</div>
      <div class="tri-card-title">Romero — Punto de inflexión</div>
      <p><strong>1985 es el año clave:</strong> Juicio a las Juntas (justicia) + Plan Austral (economía). Preguntan por qué el Plan falló: puja distributiva + gasto público acumulado.</p>
    </div>
  </div>
</div>

<div class="traps-section">
  <div class="traps-title">⚠ Trampas recurrentes en los exámenes</div>
  <div class="trap-item"><div class="trap-dot"></div><div class="trap-text"><strong>Golpe vs. Interrupción institucional:</strong> Frondizi 1962 es el ejemplo favorito. Lo sacan militares, pero asume Guido por acefalía → se mantiene "fachada" de legalidad, no hubo cambio de régimen.</div></div>
  <div class="trap-item"><div class="trap-dot"></div><div class="trap-text"><strong>Estado vs. Gobierno:</strong> confundirlos es un error básico. El Estado es permanente, el gobierno cambia.</div></div>
  <div class="trap-item"><div class="trap-dot"></div><div class="trap-text"><strong>Doble Estado en la dictadura:</strong> coexiste un Estado administrativo visible y un Estado clandestino (centros de detención). No es solo represión, es un sistema paralelo.</div></div>
  <div class="trap-item"><div class="trap-dot"></div><div class="trap-text"><strong>Genocidio y grupos protegidos:</strong> la Convención de 1948 protege grupos nacionales, étnicos, raciales y religiosos. Los grupos <em>políticos</em> quedaron afuera.</div></div>
  <div class="trap-item"><div class="trap-dot"></div><div class="trap-text"><strong>Poliarquía ≠ democracia perfecta:</strong> es la definición <em>mínima</em>. Una democracia puede ser poliarquía aunque tenga inequidad económica.</div></div>
</div>

<nav>
  <a href="#s1">1. Estado</a>
  <a href="#s2">2. Nación</a>
  <a href="#s3">3. Sociedad</a>
  <a href="#s4">4. Regímenes</a>
  <a href="#s5">5. Golpes y Terror</a>
  <a href="#s6">6. Argentina 66–83</a>
  <a href="#s7">7. Transición y DDHH</a>
</nav>

<!-- ========== SECCIÓN 1 ========== -->
<section class="section" id="s1">
  <div class="section-header">
    <div class="section-num" style="background:var(--blue-bg);color:var(--blue);">1</div>
    <div><h2>Estado y sus tipos</h2><p>Weber · Hobbes · Legitimidad · Modelos históricos</p></div>
  </div>

  <div class="subsection">
    <div class="subsection-title">Definición central — Weber</div>
    <div class="cards">
      <div class="card" style="border-color:var(--blue-dim)">
        <div class="card-label" style="color:var(--blue)">Definición</div>
        <div class="card-title">Monopolio de la violencia legítima</div>
        <div class="card-body">Comunidad humana que, dentro de un territorio, tiene el monopolio del uso <em>legítimo</em> de la fuerza. Solo el Estado puede usar la fuerza de manera legal y aceptada (policía, ejército).</div>
      </div>
      <div class="card" style="border-color:var(--blue-dim)">
        <div class="card-label" style="color:var(--blue)">Elementos constitutivos</div>
        <div class="card-title">Territorio · Población · Soberanía · Normas</div>
        <div class="card-body">Esta definición "jurídica" incluye modelos tan distintos como el liberal, el fascista o el socialista porque todos comparten estos cuatro elementos básicos.</div>
      </div>
      <div class="card" style="border-color:var(--blue-dim)">
        <div class="card-label" style="color:var(--blue)">Distinción clave</div>
        <div class="card-title">Estado ≠ Gobierno</div>
        <div class="card-body">El Estado es la estructura permanente. El gobierno es quien lo administra de forma temporal. Los gobiernos cambian; el Estado continúa.</div>
      </div>
    </div>
    <div class="keybox blue"><strong>Hobbes:</strong> el Estado surge para evitar la "guerra de todos contra todos". Sin poder común, los individuos viven en conflicto permanente (estado de naturaleza).</div>
    <div class="keybox blue"><strong>Estado fallido:</strong> cuando grupos fuera del Estado ejercen violencia en su territorio, el Estado pierde el monopolio y su autoridad se debilita.</div>
    <div class="exam-tip">Siempre que pregunten por Weber, mencioná los dos elementos: territorio + monopolio de la violencia LEGÍTIMA (el "legítima" es lo que diferencia al Estado).</div>
  </div>

  <div class="subsection">
    <div class="subsection-title">Los 3 tipos de legitimidad — Weber</div>
    <div class="cards">
      <div class="card" style="border-color:#2a2060">
        <div class="card-label" style="color:var(--purple)">Tradicional</div>
        <div class="card-title">Costumbre y hábito</div>
        <div class="card-body">Se obedece porque "siempre fue así". La costumbre hereditaria valida la autoridad. Ej.: monarquías antiguas.</div>
      </div>
      <div class="card" style="border-color:#3a1a10">
        <div class="card-label" style="color:var(--coral)">Carismática</div>
        <div class="card-title">Magnetismo del líder</div>
        <div class="card-body">Obediencia por confianza en las cualidades personales extraordinarias de un líder. Sin ese líder, la legitimidad se desvanece. Ej.: Perón, Yrigoyen.</div>
      </div>
      <div class="card" style="border-color:var(--blue-dim)">
        <div class="card-label" style="color:var(--blue)">Legal-racional</div>
        <div class="card-title">Normas e instituciones</div>
        <div class="card-body">Se obedece la ley, no la persona. Las normas son racionales y creadas democráticamente. Base de los Estados modernos democráticos.</div>
      </div>
    </div>
    <div class="exam-tip">La dictadura puede tener legitimidad carismática o tradicional, pero nunca legal-racional (porque no respeta las normas).</div>
  </div>

  <div class="subsection">
    <div class="subsection-title">Modelos históricos de Estado</div>
    <div class="table-wrap">
      <table>
        <thead><tr><th>Tipo</th><th>Características centrales</th><th>Surgimiento</th><th>Economía</th></tr></thead>
        <tbody>
          <tr><td>Liberal</td><td>División de poderes, derechos individuales, representación, Estado limitado</td><td>Reacción al absolutismo. Revoluciones s. XVIII</td><td>Libre mercado, mínima intervención</td></tr>
          <tr><td>Socialista</td><td>Partido único, poder concentrado, busca igualdad. Sin libertades políticas</td><td>Crítica al capitalismo liberal. URSS</td><td>Estado controla la economía</td></tr>
          <tr><td>Fascista</td><td>Nacionalismo extremo, totalitario, individuo subordinado al Estado</td><td>Reacción al liberalismo. Entreguerras</td><td>Corporativista: interviene pero defiende propiedad privada</td></tr>
          <tr><td>De Bienestar</td><td>Capitalismo + políticas sociales (salud, educación, jubilaciones)</td><td>Post Segunda Guerra Mundial</td><td>Capitalismo regulado + Estado proveedor de servicios</td></tr>
          <tr><td>Neoliberal</td><td>Achica el Estado, privatiza, desregula, abre el comercio</td><td>Crisis del Bienestar en los 70. AL en los 90</td><td>El mercado asigna recursos. Reduce gasto social</td></tr>
          <tr><td>Plurinacional</td><td>Reconoce múltiples pueblos, pluralismo jurídico, autogobierno indígena</td><td>"Ola rosa" latinoamericana s. XXI. Bolivia, Ecuador</td><td>Variable según el país</td></tr>
        </tbody>
      </table>
    </div>
    <div class="keybox amber"><strong>Lógica de surgimiento:</strong> cada modelo aparece como reacción al anterior. Liberal → absolutismo. Fascista/socialista → liberalismo. Bienestar → fascismo y crisis. Neoliberal → bienestar. Plurinacional → neoliberalismo.</div>
    <div class="exam-tip">En los exámenes aparece mucho la comparación Estado de Bienestar vs. Neoliberal. Clave: el de Bienestar <em>interviene</em> para dar derechos sociales; el Neoliberal se <em>retira</em>, privatiza y busca equilibrio fiscal.</div>
  </div>

  <div class="subsection">
    <div class="subsection-title">Preguntas guía</div>
    <div class="accordion" id="acc-estado"></div>
  </div>

  <div class="quiz-launcher">
    <button class="quiz-btn" onclick="openQuiz('estado')">
      <span class="btn-icon">⚡</span> QUIZ MÓDULO 1 — Estado
    </button>
    <div class="quiz-stats-mini" id="stats-estado"></div>
  </div>
</section>

<!-- ========== SECCIÓN 2 ========== -->
<section class="section" id="s2">
  <div class="section-header">
    <div class="section-num" style="background:var(--teal-bg);color:var(--teal);">2</div>
    <div><h2>Nación e identidad</h2><p>Gellner · Anderson · Hobsbawm · Construcción de la nación argentina</p></div>
  </div>

  <div class="subsection">
    <div class="subsection-title">La diferencia fundamental</div>
    <div class="cards">
      <div class="card" style="border-color:var(--blue-dim)">
        <div class="card-label" style="color:var(--blue)">Estado</div>
        <div class="card-title">Institución política formal</div>
        <div class="card-body">Estructura con territorio, normas y autoridad. Es institucional y jurídico. Puede existir sin nación definida.</div>
      </div>
      <div class="card" style="border-color:#0a3d20">
        <div class="card-label" style="color:var(--teal)">Nación</div>
        <div class="card-title">Identidad y pertenencia</div>
        <div class="card-body">Comunidad imaginada con lengua, historia, cultura y símbolos compartidos. No siempre tiene Estado propio.</div>
      </div>
    </div>
    <div class="keybox teal"><strong>Ejemplo clave:</strong> el pueblo kurdo tiene nación (identidad, lengua, cultura) pero no tiene Estado propio. Argentina en cambio formó el Estado <em>antes</em> que la nación.</div>
  </div>

  <div class="subsection">
    <div class="subsection-title">¿Qué es la nación? — dos concepciones</div>
    <div class="cards">
      <div class="card">
        <div class="card-label" style="color:var(--coral)">Concepción objetiva</div>
        <div class="card-title">Rasgos comunes</div>
        <div class="card-body">La nación se define por rasgos compartidos: lengua, territorio, etnia, religión, cultura.</div>
      </div>
      <div class="card">
        <div class="card-label" style="color:var(--purple)">Concepción constructivista</div>
        <div class="card-title">Construcción social moderna</div>
        <div class="card-body"><strong>Gellner, Anderson y Hobsbawm:</strong> la nación NO es natural ni eterna. Es una invención moderna (s. XIX) ligada al Estado moderno, al capitalismo y a la imprenta.</div>
      </div>
    </div>
    <div class="keybox purple"><strong>Anderson — "Comunidad imaginada":</strong> los miembros de una nación nunca se conocen todos entre sí, pero se <em>imaginan</em> como comunidad. La imprenta y los periódicos fueron clave.</div>
    <div class="keybox purple"><strong>Hobsbawm — "Tradiciones inventadas":</strong> muchas tradiciones que parecen antiguas fueron inventadas en el s. XIX para crear cohesión nacional.</div>
  </div>

  <div class="subsection">
    <div class="subsection-title">Construcción de la nación argentina — cronología</div>
    <div class="timeline">
      <div class="tl-item">
        <div class="tl-left"><div class="tl-dot" style="background:var(--teal)"></div><div class="tl-line-seg"></div></div>
        <div class="tl-content"><div class="tl-year" style="color:var(--teal)">1853–1862</div><div class="tl-title">Organización del Estado</div><div class="tl-text">Constitución de 1853. Consolidación en 1862 (Mitre). El Estado se forma <em>antes</em> que la nación — al revés de Europa.</div></div>
      </div>
      <div class="tl-item">
        <div class="tl-left"><div class="tl-dot" style="background:var(--teal)"></div><div class="tl-line-seg"></div></div>
        <div class="tl-content"><div class="tl-year" style="color:var(--teal)">1880</div><div class="tl-title">Consolidación del Estado nacional</div><div class="tl-text">Federalización de Buenos Aires. El Estado controla definitivamente el territorio y el monopolio de la fuerza.</div></div>
      </div>
      <div class="tl-item">
        <div class="tl-left"><div class="tl-dot" style="background:var(--teal)"></div><div class="tl-line-seg"></div></div>
        <div class="tl-content"><div class="tl-year" style="color:var(--teal)">1880–1910</div><div class="tl-title">Construcción de la identidad nacional</div><div class="tl-text">Alta inmigración masiva → urgencia de crear identidad. Herramientas: educación pública (Ley 1420), fiestas patrias, historia oficial, símbolos nacionales, servicio militar obligatorio.</div></div>
      </div>
      <div class="tl-item">
        <div class="tl-left"><div class="tl-dot" style="background:var(--teal)"></div></div>
        <div class="tl-content"><div class="tl-year" style="color:var(--teal)">Tensión central</div><div class="tl-title">"Crisol de razas" vs. identidad criolla</div><div class="tl-text">"Crisol de razas" proponía integrar a los inmigrantes. La identidad criolla/hispánica propugnaba la continuidad de la cultura previa. Hacia 1910 prevalece la segunda.</div></div>
      </div>
    </div>
    <div class="exam-tip">Argentina invirtió el orden europeo: primero el Estado, después la nación (mediante políticas públicas de educación y símbolos patrios).</div>
  </div>

  <div class="subsection">
    <div class="subsection-title">Preguntas guía</div>
    <div class="accordion" id="acc-nacion"></div>
  </div>

  <div class="quiz-launcher">
    <button class="quiz-btn" onclick="openQuiz('nacion')">
      <span class="btn-icon">⚡</span> QUIZ MÓDULO 2 — Nación
    </button>
    <div class="quiz-stats-mini" id="stats-nacion"></div>
  </div>
</section>

<!-- ========== SECCIÓN 3 ========== -->
<section class="section" id="s3">
  <div class="section-header">
    <div class="section-num" style="background:var(--purple-bg);color:var(--purple);">3</div>
    <div><h2>Sociedad, ciudadanía y acción social</h2><p>Weber · Bourdieu · Ciudadanía · Sociedad civil · Actores sociales</p></div>
  </div>

  <div class="subsection">
    <div class="subsection-title">Persona · Ciudadano · Ciudadanía</div>
    <div class="cards">
      <div class="card">
        <div class="card-label" style="color:var(--blue)">Persona</div>
        <div class="card-title">Derechos humanos universales</div>
        <div class="card-body">Todo ser humano tiene derechos por el solo hecho de existir, independientemente del Estado al que pertenezca.</div>
      </div>
      <div class="card">
        <div class="card-label" style="color:var(--teal)">Ciudadano</div>
        <div class="card-title">Derechos otorgados por el Estado</div>
        <div class="card-body">Quien posee derechos específicos reconocidos por un Estado particular. Cambia según el país y la época.</div>
      </div>
      <div class="card">
        <div class="card-label" style="color:var(--coral)">Ciudadanía</div>
        <div class="card-title">"El derecho a tener derechos"</div>
        <div class="card-body">Proceso histórico de expansión y disputa. Cada ampliación modifica la distribución del poder social. No es algo dado, se conquista.</div>
      </div>
    </div>
  </div>

  <div class="subsection">
    <div class="subsection-title">Acción social — los 4 tipos de Weber</div>
    <div class="cards">
      <div class="card"><div class="card-label" style="color:var(--purple)">Tradicional</div><div class="card-body">Por costumbre. "Siempre se hizo así." La tradición guía la conducta sin reflexión racional.</div></div>
      <div class="card"><div class="card-label" style="color:var(--coral)">Afectiva</div><div class="card-body">Motivada por emociones y sentimientos del momento. Reacciones afectivas, pasionales.</div></div>
      <div class="card"><div class="card-label" style="color:var(--teal)">Racional con arreglo a valores</div><div class="card-body">Guiada por principios éticos o morales independientemente de las consecuencias. El valor en sí mismo orienta la acción.</div></div>
      <div class="card"><div class="card-label" style="color:var(--blue)">Racional con arreglo a fines</div><div class="card-body">Cálculo racional de medios y fines. La más "moderna" para Weber. Propia del capitalismo y la burocracia.</div></div>
    </div>
    <div class="keybox purple"><strong>Definición:</strong> acción social = conducta con <em>sentido</em> para quien la realiza, <em>orientada hacia otros</em>. No toda conducta es acción social (ej.: tropezar no lo es).</div>
  </div>

  <div class="subsection">
    <div class="subsection-title">Estratificación social — Weber y Bourdieu</div>
    <div class="table-wrap">
      <table>
        <thead><tr><th>Dimensión</th><th>Concepto</th><th>Definición</th></tr></thead>
        <tbody>
          <tr><td>Económica (Weber)</td><td>Clases</td><td>Posición según acceso a bienes y al mercado. Determinada por la propiedad.</td></tr>
          <tr><td>Social (Weber)</td><td>Estamentos</td><td>Estilo de vida y prestigio social. No se reduce a lo económico.</td></tr>
          <tr><td>Política (Weber)</td><td>Partidos</td><td>Disputa por influir en el poder colectivo y dirigir la acción.</td></tr>
          <tr><td>Capital (Bourdieu)</td><td>Campos y capitales</td><td>Posiciones dependen de capital económico, cultural y social. La trayectoria importa.</td></tr>
        </tbody>
      </table>
    </div>
  </div>

  <div class="subsection">
    <div class="subsection-title">Sociedad civil y actores sociales</div>
    <div class="keybox"><strong>Sociedad civil:</strong> espacio de organización de ciudadanos <em>fuera</em> del Estado. Incluye sindicatos, ONGs, iglesias, medios. Su función central es <strong>limitar y controlar el poder estatal</strong>.</div>
    <div class="keybox teal"><strong>El Cordobazo (1969):</strong> ejemplo emblemático de acción conjunta. El movimiento obrero y el estudiantil se unieron contra la dictadura de Onganía. Demostró que la acción colectiva puede cambiar el rumbo político.</div>
  </div>

  <div class="quiz-launcher">
    <button class="quiz-btn" onclick="openQuiz('sociedad')">
      <span class="btn-icon">⚡</span> QUIZ MÓDULO 3 — Sociedad y ciudadanía
    </button>
    <div class="quiz-stats-mini" id="stats-sociedad"></div>
  </div>
</section>

<!-- ========== SECCIÓN 4 ========== -->
<section class="section" id="s4">
  <div class="section-header">
    <div class="section-num" style="background:var(--blue-bg);color:var(--blue);">4</div>
    <div><h2>Regímenes políticos y democracia</h2><p>Dahl · Poliarquía · Populismo · Federalismo</p></div>
  </div>

  <div class="subsection">
    <div class="subsection-title">Concepto de régimen político</div>
    <div class="keybox blue"><strong>Régimen político:</strong> conjunto de normas que determinan <em>cómo se accede al poder y cómo se ejerce</em>. Distinguir: régimen ≠ gobierno (el gobierno cambia dentro del mismo régimen).</div>
    <div class="keybox blue"><strong>Transición de régimen:</strong> cambio en las reglas del juego, no solo en quién gobierna. En Argentina: múltiples transiciones entre dictaduras y democracias. Desde 1983 se mantiene el régimen democrático.</div>
  </div>

  <div class="subsection">
    <div class="subsection-title">Democracia vs. Autoritarismo</div>
    <div class="table-wrap">
      <table>
        <thead><tr><th>Dimensión</th><th>Democracia</th><th>Autoritarismo</th></tr></thead>
        <tbody>
          <tr><td>Acceso al poder</td><td>Elecciones libres, competitivas, con incertidumbre real sobre el resultado</td><td>No surge de elecciones; concentración en una persona o grupo</td></tr>
          <tr><td>Límites al poder</td><td>Estado de derecho, división de poderes, control recíproco</td><td>No está limitado por leyes ni instituciones</td></tr>
          <tr><td>Derechos</td><td>Garantía de derechos civiles y políticos</td><td>No garantiza libertades políticas. Suprime la oposición</td></tr>
          <tr><td>Alternancia</td><td>Posibilidad real de que el gobierno pierda y deje el poder</td><td>Sin alternancia; el poder se perpetúa</td></tr>
        </tbody>
      </table>
    </div>
  </div>

  <div class="subsection">
    <div class="subsection-title">La Poliarquía de Robert Dahl — los 6 atributos</div>
    <div class="keybox blue"><strong>Poliarquía:</strong> definición <em>mínima y procedimental</em> de democracia. Se centra en reglas e instituciones (no en igualdad económica o social). Sirve para distinguir democracia de autoritarismo.</div>
    <div class="pills">
      <span class="pill pill-blue">1. Sufragio universal, igual y secreto</span>
      <span class="pill pill-blue">2. Elecciones limpias, periódicas y competitivas</span>
      <span class="pill pill-blue">3. Ejercicio del poder sin condicionamientos externos</span>
      <span class="pill pill-blue">4. Alternancia real entre partidos</span>
      <span class="pill pill-blue">5. Pluralidad de la oferta electoral</span>
      <span class="pill pill-blue">6. Libertad de expresión e información diversa</span>
    </div>
    <div class="exam-tip">En el examen pueden darte una situación hipotética y preguntarte si es poliarquía. Revisá uno por uno: ¿hay sufragio universal? ¿son las elecciones limpias? ¿hay libertad de expresión? El que falta es la trampa.</div>
  </div>

  <div class="subsection">
    <div class="subsection-title">Populismo — definición y características</div>
    <div class="cards">
      <div class="card"><div class="card-label" style="color:var(--amber)">¿Qué es?</div><div class="card-body">Concepto polémico y polisémico: puede ser régimen, liderazgo, ideología, discurso o cultura política. No tiene una sola definición.</div></div>
      <div class="card"><div class="card-label" style="color:var(--amber)">Rasgo central</div><div class="card-body">Construcción del "pueblo" vs. la "élite corrupta". División entre "nosotros" (el pueblo) y "ellos" (el establishment). El líder se presenta como la voz del pueblo.</div></div>
      <div class="card"><div class="card-label" style="color:var(--amber)">Relación con democracia</div><div class="card-body">Puede coexistir con elecciones, pero tiende a <em>erosionar</em> la calidad democrática: concentra poder en el Ejecutivo, debilita la división de poderes.</div></div>
      <div class="card"><div class="card-label" style="color:var(--amber)">Casos argentinos</div><div class="card-body"><strong>Yrigoyen:</strong> liderazgo carismático, confrontación con el régimen oligárquico. <strong>Perón:</strong> partido propio desde el Estado, mayor control de medios y búsqueda de permanencia.</div></div>
    </div>
  </div>

  <div class="subsection">
    <div class="subsection-title">Federalismo argentino</div>
    <div class="table-wrap">
      <table>
        <thead><tr><th>Modelo</th><th>Descripción</th><th>Ejemplo</th></tr></thead>
        <tbody>
          <tr><td>Coming together</td><td>Unidades independientes se unen voluntariamente para formar un Estado federal</td><td>Estados Unidos</td></tr>
          <tr><td>Holding together</td><td>Un Estado unitario se federaliza para mantener la unidad ante presiones centrífugas</td><td>España, India</td></tr>
          <tr><td>Putting together</td><td>Un poder central impone la unión territorial sobre unidades que no la eligieron</td><td>Unión Soviética</td></tr>
        </tbody>
      </table>
    </div>
  </div>

  <div class="quiz-launcher">
    <button class="quiz-btn" onclick="openQuiz('regimenes')">
      <span class="btn-icon">⚡</span> QUIZ MÓDULO 4 — Regímenes y democracia
    </button>
    <div class="quiz-stats-mini" id="stats-regimenes"></div>
  </div>
</section>

<!-- ========== SECCIÓN 5 ========== -->
<section class="section" id="s5">
  <div class="section-header">
    <div class="section-num" style="background:var(--red-bg);color:var(--red);">5</div>
    <div><h2>Golpes de Estado, terrorismo y genocidio</h2><p>Deich · Statello · Lamarque · Lemkin</p></div>
  </div>

  <div class="subsection">
    <div class="subsection-title">Golpes de Estado — tipología</div>
    <div class="keybox red"><strong>Definición:</strong> toma del poder por la fuerza, rompiendo el orden constitucional. Es <em>siempre ilegal</em> y <em>siempre implica violencia</em> (aunque varíe su grado).</div>
    <div class="cards">
      <div class="card" style="border-color:#3a1010"><div class="card-label" style="color:var(--red)">Golpe militar</div><div class="card-body">Las Fuerzas Armadas desplazan al gobierno. Caso más frecuente en América Latina durante el s. XX.</div></div>
      <div class="card" style="border-color:#3a1010"><div class="card-label" style="color:var(--red)">Golpe civil</div><div class="card-body">Actores civiles (empresarios, sectores políticos, medios) promueven o lideran la ruptura con participación militar.</div></div>
      <div class="card" style="border-color:#3a1010"><div class="card-label" style="color:var(--red)">Autogolpe</div><div class="card-body">El propio gobernante concentra poder vulnerando el orden constitucional. Ej.: Fujimori en Perú (1992).</div></div>
      <div class="card" style="border-color:#2a1a50"><div class="card-label" style="color:var(--purple)">Interrupción institucional</div><div class="card-body">El presidente abandona el cargo sin golpe militar clásico. Sin cambio de régimen. Ej.: De la Rúa 2001, Frondizi 1962.</div></div>
    </div>
    <div class="exam-tip"><strong>Frondizi 1962:</strong> los militares lo presionaron para renunciar, pero asumió el presidente provisional del Senado (Guido) siguiendo la ley de acefalía. Es una interrupción institucional, no un golpe clásico.</div>
  </div>

  <div class="subsection">
    <div class="subsection-title">Terrorismo político</div>
    <div class="cards">
      <div class="card"><div class="card-label" style="color:var(--amber)">Terrorismo</div><div class="card-title">Violencia política deliberada</div><div class="card-body">Uso de violencia deliberada contra civiles para generar miedo y lograr objetivos políticos. Tiene una dimensión <em>comunicativa</em>: el acto es un mensaje.</div></div>
      <div class="card" style="border-color:#3a1010"><div class="card-label" style="color:var(--red)">Terrorismo de Estado</div><div class="card-title">"Doble Estado"</div><div class="card-body">El propio Estado usa terror sistemático. Coexiste un Estado administrativo visible y un Estado clandestino (centros de detención, grupos parapoliciales).</div></div>
    </div>
    <div class="keybox amber"><strong>Las 4 olas del terrorismo (Rapoport):</strong> 1) Anarquista (fines s. XIX) → 2) Anticolonial (post WWII) → 3) Nueva izquierda (60-70s) → 4) Religiosa (desde los 80s). Argentina se enmarca principalmente en la tercera ola.</div>
  </div>

  <div class="subsection">
    <div class="subsection-title">Genocidio — Lemkin y la Convención de 1948</div>
    <div class="table-wrap">
      <table>
        <thead><tr><th>Elemento</th><th>Definición / Detalle</th></tr></thead>
        <tbody>
          <tr><td>Concepto (Lemkin)</td><td>Destrucción de grupos como tales, no de individuos aislados. Fenómeno moderno, planificado y organizado. Incluye dimensión cultural.</td></tr>
          <tr><td>Dolus specialis</td><td>Intención específica de destruir total o parcialmente a un grupo. Sin esta intención, puede ser otro crimen pero no genocidio.</td></tr>
          <tr><td>Grupos protegidos</td><td>Nacional, étnico, racial y religioso. Los grupos <em>políticos y sociales</em> quedaron <strong>excluidos</strong> de la Convención de 1948.</td></tr>
          <tr><td>Antecedentes</td><td>Juicios de Núremberg (1945) + Resolución ONU 1946 → Convención del Genocidio 1948.</td></tr>
          <tr><td>Debate argentino</td><td>Si la dictadura del 76 fue genocidio: los grupos políticos no están en la Convención, pero las Cs. Sociales debaten si fue genocidio político o de clase.</td></tr>
        </tbody>
      </table>
    </div>
    <div class="exam-tip">Los grupos políticos NO están en la Convención de 1948. Esta distinción es una trampa frecuente.</div>
  </div>

  <div class="quiz-launcher">
    <button class="quiz-btn" onclick="openQuiz('violencia')">
      <span class="btn-icon">⚡</span> QUIZ MÓDULO 5 — Golpes, Terror y Genocidio
    </button>
    <div class="quiz-stats-mini" id="stats-violencia"></div>
  </div>
</section>

<!-- ========== SECCIÓN 6 ========== -->
<section class="section" id="s6">
  <div class="section-header">
    <div class="section-num" style="background:#1a0800;color:var(--coral);">6</div>
    <div><h2>Argentina 1966–1983</h2><p>Romero Caps. VI y VII · Dictaduras · Proceso · Malvinas</p></div>
  </div>

  <div class="subsection">
    <div class="subsection-title">Golpes en Argentina — cronología completa</div>
    <div class="timeline">
      <div class="tl-item"><div class="tl-left"><div class="tl-dot" style="background:var(--red)"></div><div class="tl-line-seg"></div></div><div class="tl-content"><div class="tl-year" style="color:var(--red)">1930</div><div class="tl-title">Primer golpe — Uriburu</div><div class="tl-text">Derroca a Yrigoyen. Comienza la "Década Infame". Carácter transitorio.</div></div></div>
      <div class="tl-item"><div class="tl-left"><div class="tl-dot" style="background:var(--red)"></div><div class="tl-line-seg"></div></div><div class="tl-content"><div class="tl-year" style="color:var(--red)">1943</div><div class="tl-title">Golpe del GOU</div><div class="tl-text">Contexto de la Segunda Guerra Mundial. De este proceso emerge Perón como figura política central.</div></div></div>
      <div class="tl-item"><div class="tl-left"><div class="tl-dot" style="background:var(--red)"></div><div class="tl-line-seg"></div></div><div class="tl-content"><div class="tl-year" style="color:var(--red)">1955</div><div class="tl-title">Revolución Libertadora</div><div class="tl-text">Derroca a Perón. Inicia la proscripción del peronismo que dura hasta 1973.</div></div></div>
      <div class="tl-item"><div class="tl-left"><div class="tl-dot" style="background:var(--amber)"></div><div class="tl-line-seg"></div></div><div class="tl-content"><div class="tl-year" style="color:var(--amber)">1962</div><div class="tl-title">Caso Frondizi — INTERRUPCIÓN institucional</div><div class="tl-text">Presión militar, pero asume el titular del Senado (Guido) por acefalía. No hubo cambio de régimen.</div></div></div>
      <div class="tl-item"><div class="tl-left"><div class="tl-dot" style="background:var(--red)"></div><div class="tl-line-seg"></div></div><div class="tl-content"><div class="tl-year" style="color:var(--red)">1966</div><div class="tl-title">Revolución Argentina — Onganía</div><div class="tl-text">Golpe contra Illia. Primer golpe con intención de permanencia. Genera el Cordobazo (1969) como respuesta.</div></div></div>
      <div class="tl-item"><div class="tl-left"><div class="tl-dot" style="background:var(--teal)"></div><div class="tl-line-seg"></div></div><div class="tl-content"><div class="tl-year" style="color:var(--teal)">1973</div><div class="tl-title">Retorno democrático — Cámpora / Perón</div><div class="tl-text">GAN de Lanusse. Perón vuelve del exilio. Cámpora → Perón → Isabel. Alta violencia política: Montoneros, ERP, Triple A.</div></div></div>
      <div class="tl-item"><div class="tl-left"><div class="tl-dot" style="background:var(--red)"></div><div class="tl-line-seg"></div></div><div class="tl-content"><div class="tl-year" style="color:var(--red)">24/03/1976</div><div class="tl-title">El Proceso — Junta Militar</div><div class="tl-text">Videla – Massera – Agosti. Última y más brutal dictadura. Terrorismo de Estado sistemático. Doble Estado.</div></div></div>
      <div class="tl-item"><div class="tl-left"><div class="tl-dot" style="background:var(--amber)"></div><div class="tl-line-seg"></div></div><div class="tl-content"><div class="tl-year" style="color:var(--amber)">1982</div><div class="tl-title">Guerra de Malvinas</div><div class="tl-text">Galtieri busca apoyo social con la guerra. Derrota completa ante el Reino Unido. Crisis terminal del régimen.</div></div></div>
      <div class="tl-item"><div class="tl-left"><div class="tl-dot" style="background:var(--teal)"></div></div><div class="tl-content"><div class="tl-year" style="color:var(--teal)">1983</div><div class="tl-title">Retorno democrático — Alfonsín</div><div class="tl-text">Triunfo de la UCR sobre el peronismo. La democracia como expectativa social ampliamente compartida.</div></div></div>
    </div>
  </div>

  <div class="subsection">
    <div class="subsection-title">La última dictadura (1976–1983) — ejes clave</div>
    <div class="cards">
      <div class="card" style="border-color:#3a1010"><div class="card-label" style="color:var(--red)">Terrorismo de Estado</div><div class="card-body">Centros clandestinos de detención (CCD), desaparición forzada, tortura sistemática. El objetivo no era solo eliminar opositores sino generar terror en toda la sociedad.</div></div>
      <div class="card" style="border-color:#3a1010"><div class="card-label" style="color:var(--red)">Doble Estado</div><div class="card-body">Coexistía un Estado administrativo visible (ministerios, leyes) con un Estado clandestino (centros de detención, grupos de tareas). La fachada de legalidad cubría el terror.</div></div>
      <div class="card" style="border-color:#4a2a00"><div class="card-label" style="color:var(--amber)">Política económica — Martínez de Hoz</div><div class="card-body">Apertura financiera + "tablita" cambiaria (dólar barato) → "plata dulce" y "bicicleta" financiera → desindustrialización → deuda externa → crisis 1980-82.</div></div>
      <div class="card" style="border-color:#4a2a00"><div class="card-label" style="color:var(--amber)">Malvinas (1982)</div><div class="card-body">Galtieri buscó apoyo social con la guerra. Apoyo inicial masivo. Derrota militar completa → deslegitimó definitivamente al régimen.</div></div>
    </div>
    <div class="keybox red"><strong>Paradoja central del Proceso:</strong> el régimen decía "achicar el Estado" pero usó al Estado para el terror y el beneficio de grupos económicos concentrados.</div>
  </div>

  <div class="quiz-launcher">
    <button class="quiz-btn" onclick="openQuiz('argentina')">
      <span class="btn-icon">⚡</span> QUIZ MÓDULO 6 — Argentina 1966–1983
    </button>
    <div class="quiz-stats-mini" id="stats-argentina"></div>
  </div>
</section>

<!-- ========== SECCIÓN 7 ========== -->
<section class="section" id="s7">
  <div class="section-header">
    <div class="section-num" style="background:var(--teal-bg);color:var(--teal);">7</div>
    <div><h2>Transición democrática y Derechos Humanos</h2><p>Alfonsín · 1985 como año clave · Derechos humanos · Kant · Montero</p></div>
  </div>

  <div class="subsection">
    <div class="subsection-title">Conceptos de la transición</div>
    <div class="cards">
      <div class="card"><div class="card-label" style="color:var(--blue)">Transición</div><div class="card-title">Cambio de régimen</div><div class="card-body">Período de cambio de un régimen autoritario a uno democrático. El resultado es incierto: puede fracasar y volver al autoritarismo.</div></div>
      <div class="card"><div class="card-label" style="color:var(--teal)">Consolidación</div><div class="card-title">La democracia "se normaliza"</div><div class="card-body">La democracia se estabiliza: actores clave aceptan las reglas del juego como "el único juego posible". Se descarta la opción autoritaria.</div></div>
    </div>
  </div>

  <div class="subsection">
    <div class="subsection-title">Transiciones argentinas comparadas</div>
    <div class="table-wrap">
      <table>
        <thead><tr><th>Dimensión</th><th>1973 (fallida)</th><th>1983 (exitosa)</th></tr></thead>
        <tbody>
          <tr><td>Contexto</td><td>Alta polarización, violencia armada, crisis del peronismo en el poder</td><td>Derrota en Malvinas, descrédito militar total, crisis económica</td></tr>
          <tr><td>Sociedad civil</td><td>Movilizada pero dividida entre proyectos radicalmente opuestos</td><td>DDHH como eje articulador, fuerte demanda democrática transversal</td></tr>
          <tr><td>Militares</td><td>Retirada negociada con poder de veto residual</td><td>Derrota de Malvinas eliminó su capacidad de negociar condiciones</td></tr>
          <tr><td>Resultado</td><td>Golpe de 1976 apenas 3 años después</td><td>Democracia que se consolida y persiste hasta hoy</td></tr>
        </tbody>
      </table>
    </div>
  </div>

  <div class="subsection">
    <div class="subsection-title">★ 1985 — El año clave (Romero)</div>
    <div class="keybox gold"><strong>Juicio a las Juntas (1985):</strong> hito histórico mundial. Argentina fue el primer país en juzgar a sus propios dictadores en democracia. Condenas a Videla, Massera y otros. Símbolo de que la democracia podía hacer justicia.</div>
    <div class="keybox gold"><strong>Plan Austral (1985):</strong> plan de estabilización de Alfonsín para frenar la inflación. Éxito inicial pero fracasó porque no pudo resolver la <em>puja distributiva</em> ni el gasto público acumulado. La inflación volvió con más fuerza.</div>
    <div class="exam-tip">Cuando pregunten por 1985, mencioná AMBAS dimensiones: justicia (Juicio a las Juntas) + economía (Plan Austral). La pregunta puede pedir que las articulés.</div>
  </div>

  <div class="subsection">
    <div class="subsection-title">Gobierno de Alfonsín (1983–1989) — tensiones</div>
    <div class="cards">
      <div class="card"><div class="card-label" style="color:var(--teal)">Ilusión democrática</div><div class="card-body">El triunfo de Alfonsín se sustentó en el valor de la democracia por sobre los partidos. Gran expectativa social que luego chocó con la realidad.</div></div>
      <div class="card"><div class="card-label" style="color:var(--red)">Cuestión militar</div><div class="card-body">Presión de los "carapintadas" (levantamientos de 1987, 1988). Alfonsín cede: Ley de Punto Final y Ley de Obediencia Debida. Crisis de legitimidad.</div></div>
      <div class="card"><div class="card-label" style="color:var(--amber)">Crisis económica</div><div class="card-body">Plan Austral (1985): éxito inicial, fracaso posterior. Hiperinflación de 1989. Alfonsín entrega el poder a Menem antes de tiempo.</div></div>
      <div class="card"><div class="card-label" style="color:var(--purple)">Cuestión sindical</div><div class="card-body">La CGT realizó 13 paros generales contra el gobierno radical.</div></div>
    </div>
  </div>

  <div class="subsection">
    <div class="subsection-title">Derechos Humanos — Capítulo 14 (Montero)</div>
    <div class="cards">
      <div class="card"><div class="card-label" style="color:var(--purple)">Declaración Universal 1948</div><div class="card-body">Post Segunda Guerra Mundial. Los DDHH pasan a ser objeto del derecho internacional. Punto de inflexión histórico.</div></div>
      <div class="card"><div class="card-label" style="color:var(--purple)">Características</div><div class="card-body">Universales (para toda persona), inalienables (no se pueden quitar ni transferir), indivisibles (civiles, políticos, económicos y sociales van juntos).</div></div>
      <div class="card"><div class="card-label" style="color:var(--purple)">Kant — base filosófica</div><div class="card-body">El ser humano como "fin en sí mismo, nunca como medio". Dignidad humana inherente a toda persona por su racionalidad. También Locke: derechos naturales (vida, libertad, propiedad).</div></div>
      <div class="card"><div class="card-label" style="color:var(--purple)">3 deberes del Estado</div><div class="card-body"><strong>Respetar</strong> (no interferir), <strong>proteger</strong> (evitar abusos de terceros) y <strong>promover</strong> (garantizar acceso a derechos).</div></div>
    </div>
    <div class="keybox purple"><strong>Crímenes de lesa humanidad:</strong> incluyen genocidio, tortura o desaparición forzada cuando son parte de un plan estatal. Son <em>imprescriptibles</em> y pueden juzgarse internacionalmente (jurisdicción universal).</div>
  </div>

  <div class="quiz-launcher">
    <button class="quiz-btn" onclick="openQuiz('transicion')">
      <span class="btn-icon">⚡</span> QUIZ MÓDULO 7 — Transición y DDHH
    </button>
    <div class="quiz-stats-mini" id="stats-transicion"></div>
  </div>
</section>

<footer>
  ICSE 2026 — Guía elaborada para el Primer Parcial (08/05/2026) · Semanas 1 a 5 · con sistema de repaso espaciado
</footer>

<!-- ========== QUIZ OVERLAY ========== -->
<div class="quiz-overlay" id="quizOverlay">
  <div class="quiz-container">
    <div id="quizMainView">
      <div class="quiz-topbar">
        <div class="quiz-module-name" id="quizModuleName">MÓDULO</div>
        <div class="quiz-progress-wrap">
          <div class="quiz-progress-bar-outer">
            <div class="quiz-progress-bar-inner" id="quizProgressBar" style="width:0%"></div>
          </div>
          <div class="quiz-progress-text" id="quizProgressText">0/0</div>
        </div>
        <button class="quiz-close-btn" onclick="closeQuiz()">✕ Cerrar</button>
      </div>

      <div class="quiz-scorebar">
        <div class="score-chip correct" id="chipCorrect">✓ 0 correctas</div>
        <div class="score-chip wrong" id="chipWrong">✗ 0 errores</div>
        <div class="score-chip streak" id="chipStreak">🔥 racha: 0</div>
        <div class="score-chip total" id="chipTotal">total: 0</div>
      </div>

      <div class="quiz-card" id="quizCard">
        <div class="quiz-badge-row" id="quizBadgeRow"></div>
        <div class="quiz-question" id="quizQuestionText"></div>
        <div class="quiz-options" id="quizOptions"></div>
        <div class="quiz-feedback" id="quizFeedback"></div>
        <div class="review-countdown" id="reviewCountdown">
          <span id="countdownLabel">repasando en...</span>
          <div class="countdown-bar-outer"><div class="countdown-bar-inner" id="countdownBar" style="width:100%"></div></div>
          <span id="countdownSecs"></span>
        </div>
        <button class="quiz-next-btn" id="quizNextBtn" onclick="nextQuestion()">Siguiente →</button>
      </div>
    </div>

    <div class="quiz-results" id="quizResults">
      <div class="results-header">
        <div class="results-grade" id="resultsGrade"></div>
        <div class="results-subtitle" id="resultsSubtitle"></div>
      </div>
      <div class="results-grid" id="resultsGrid"></div>
      <div id="resultsWrongList"></div>
      <div id="resultsCorrectList"></div>
      <div class="results-suggestion" id="resultsSuggestion"></div>
      <button class="results-restart-btn" onclick="restartQuiz()">↺ Repetir este módulo</button>
      <button class="results-restart-btn" style="background:var(--bg3);border-color:var(--border);color:var(--text2);margin-top:8px;" onclick="closeQuiz()">← Volver a la guía</button>
    </div>
  </div>
</div>

<script>
// =============================================
// QUIZ DATA
// =============================================
const QUIZ_DATA = {
  estado: {
    name: "MÓDULO 1 — ESTADO",
    color: "#4a9eff",
    questions: [
      {
        q: "¿Cuál es la definición de Estado según Max Weber?",
        opts: [
          "Una organización que brinda servicios públicos a la población",
          "La comunidad humana que, dentro de un territorio, tiene el monopolio del uso legítimo de la fuerza",
          "El conjunto de instituciones que conforman el gobierno de un país",
          "Una asociación voluntaria de individuos para la vida en común"
        ],
        ans: 1,
        exp: "Weber define al Estado por el monopolio de la violencia LEGÍTIMA dentro de un territorio. Lo 'legítimo' es lo que lo diferencia de cualquier otro actor que use la fuerza."
      },
      {
        q: "¿Cuál es la diferencia fundamental entre Estado y Gobierno?",
        opts: [
          "El Estado depende del gobierno para funcionar",
          "El gobierno es permanente; el Estado cambia con las elecciones",
          "El Estado es la estructura permanente; el gobierno administra temporalmente ese Estado",
          "Son sinónimos: ambos refieren a la autoridad política"
        ],
        ans: 2,
        exp: "El Estado es la estructura permanente (territorio, normas, instituciones). El gobierno es quien la administra de forma temporal. Confundirlos es un error conceptual básico en los exámenes."
      },
      {
        q: "Según Weber, ¿en qué tipo de legitimidad se basa una dictadura militar que ejerce poder por la fuerza sin respaldo institucional?",
        opts: [
          "Legal-racional, porque dictan leyes",
          "Carismática, porque el líder militar es admirado",
          "Tradicional, porque la historia militar legitima el poder",
          "Ninguna de las tres: la dictadura carece de legitimidad"
        ],
        ans: 1,
        exp: "Una dictadura puede tener legitimidad carismática (si el líder tiene carisma) o tradicional (si hay respaldo histórico), pero nunca legal-racional porque no respeta las normas institucionales. En este caso, si ejerce poder 'por la fuerza sin respaldo institucional', lo más cercano es carismática o ninguna, dependiendo del contexto."
      },
      {
        q: "¿Qué ocurre cuando grupos armados fuera del Estado ejercen violencia en su territorio?",
        opts: [
          "El Estado se fortalece porque debe responder con más fuerza",
          "El Estado pierde el monopolio de la violencia y se convierte en un 'Estado fallido'",
          "El Estado se vuelve democrático para recuperar legitimidad",
          "Los grupos armados pasan automáticamente a ser reconocidos como gobierno"
        ],
        ans: 1,
        exp: "Si grupos ajenos al Estado ejercen violencia en su territorio, el Estado pierde su monopolio y su autoridad se debilita. Esto es lo que define a un 'Estado fallido'."
      },
      {
        q: "¿Qué tienen en común el Estado liberal, el fascista y el socialista según la definición jurídica?",
        opts: [
          "Todos garantizan los derechos individuales",
          "Todos comparten los cuatro elementos: territorio, población, soberanía y normas",
          "Todos tienen elecciones libres y periódicas",
          "Todos permiten la libre organización de partidos políticos"
        ],
        ans: 1,
        exp: "La definición jurídica de Estado es lo suficientemente abstracta para incluir modelos muy distintos. Todos comparten territorio, población, soberanía y sistema jurídico. Lo que varía es cómo organizan esos elementos."
      },
      {
        q: "¿Cuál fue el argumento de Hobbes para justificar la existencia del Estado?",
        opts: [
          "El Estado garantiza la propiedad privada y el libre mercado",
          "Sin Estado, los individuos vivirían en una 'guerra de todos contra todos'",
          "El Estado es la expresión de la voluntad divina",
          "El Estado nace del acuerdo voluntario de los ciudadanos para maximizar su felicidad"
        ],
        ans: 1,
        exp: "Hobbes argumentó que sin un poder común (el Estado), los individuos vivirían en un estado de naturaleza de conflicto permanente. El Estado surge para evitar esa 'guerra de todos contra todos'."
      },
      {
        q: "El Estado de Bienestar surge como reacción a:",
        opts: [
          "El neoliberalismo y las privatizaciones de los años 90",
          "El absolutismo monárquico del siglo XVIII",
          "El fascismo y las crisis del capitalismo, especialmente post Segunda Guerra Mundial",
          "La Revolución Soviética y el avance del comunismo en Occidente exclusivamente"
        ],
        ans: 2,
        exp: "El Estado de Bienestar surgió principalmente post Segunda Guerra Mundial para fortalecer las democracias, evitar nuevas crisis económicas como la de 1929 y contrarrestar el atractivo del comunismo. Interviene para dar derechos sociales (salud, educación, jubilaciones)."
      },
      {
        q: "El Estado Neoliberal se diferencia del Estado de Bienestar porque:",
        opts: [
          "El neoliberal interviene más en la economía para redistribuir la riqueza",
          "El neoliberal privatiza, desregula y reduce el gasto social, dejando al mercado asignar recursos",
          "El neoliberal garantiza derechos sociales pero a través del mercado",
          "El neoliberal es un modelo exclusivo de América Latina en el siglo XX"
        ],
        ans: 1,
        exp: "El Estado Neoliberal 'achica' el Estado: privatiza empresas públicas, desregula la economía, abre el comercio exterior y reduce el gasto social. El mercado debe asignar los recursos. Surge como reacción a la crisis del Estado de Bienestar en los años 70."
      }
    ]
  },
  nacion: {
    name: "MÓDULO 2 — NACIÓN E IDENTIDAD",
    color: "#3fcf8e",
    questions: [
      {
        q: "¿Cómo define Benedict Anderson a la 'nación'?",
        opts: [
          "Una entidad biológica definida por la raza y la sangre común",
          "Una comunidad imaginada, porque sus miembros nunca se conocen pero se imaginan como comunidad",
          "El conjunto de personas que habitan un mismo territorio bajo un mismo gobierno",
          "Una construcción jurídica del Estado moderno basada en la ciudadanía legal"
        ],
        ans: 1,
        exp: "Anderson acuñó el concepto de 'comunidad imaginada': los miembros de una nación nunca se conocen todos entre sí, pero cada uno tiene en su mente la imagen de su comunión. La imprenta y los periódicos fueron clave para crear ese imaginario compartido."
      },
      {
        q: "¿Qué sostiene Hobsbawm con el concepto de 'tradiciones inventadas'?",
        opts: [
          "Que las naciones existen desde tiempos inmemoriales y sus tradiciones son auténticas",
          "Que muchas tradiciones que parecen antiguas fueron creadas en el siglo XIX para generar cohesión nacional",
          "Que las naciones modernas son la continuación natural de las tribus primitivas",
          "Que las tradiciones nacionales solo son válidas si tienen más de 500 años de historia"
        ],
        ans: 1,
        exp: "Hobsbawm demostró que muchas tradiciones que se presentan como antiguas y naturales fueron en realidad inventadas (o fuertemente reinventadas) en el siglo XIX para crear cohesión nacional: himnos, banderas, rituales, historias oficiales."
      },
      {
        q: "¿Por qué en Argentina el proceso fue al revés que en Europa respecto de Estado y Nación?",
        opts: [
          "Porque Argentina primero tuvo nación indígena y después organizó el Estado",
          "Porque el Estado argentino se formó antes de que existiera una identidad nacional consolidada",
          "Porque en Europa la nación llegó después que el Estado en todos los casos",
          "Porque en Argentina la nación fue creada por los inmigrantes sin intervención estatal"
        ],
        ans: 1,
        exp: "En Europa, generalmente la nación (lengua, cultura, identidad común) preexistía al Estado. En Argentina, las élites criollas construyeron el Estado (1853-1880) antes de que hubiera una identidad nacional. Luego el Estado construyó la nación 'desde arriba' con políticas de educación, símbolos y ceremonias."
      },
      {
        q: "¿Qué herramientas utilizó el Estado argentino para construir la identidad nacional ante la oleada inmigratoria de 1880-1910?",
        opts: [
          "Prohibición de idiomas extranjeros y expulsión de inmigrantes que no se asimilaran",
          "Educación pública (Ley 1420), fiestas patrias, historia oficial, símbolos nacionales y servicio militar obligatorio",
          "Otorgamiento automático de ciudadanía a todos los inmigrantes europeos",
          "Creación de colonias agrícolas separadas por nacionalidad para preservar las culturas originales"
        ],
        ans: 1,
        exp: "El Estado argentino usó la escuela pública laica y gratuita (Ley 1420), las fiestas patrias, la historia oficial, los símbolos nacionales (bandera, himno) y el servicio militar obligatorio para integrar a la enorme masa inmigratoria y crear una identidad compartida."
      },
      {
        q: "¿Cuál es la diferencia entre la concepción objetiva y la constructivista de la nación?",
        opts: [
          "La objetiva ve la nación como una invención moderna; la constructivista como algo natural y permanente",
          "La objetiva define la nación por rasgos compartidos (lengua, etnia, cultura); la constructivista la ve como una construcción histórica moderna",
          "Son dos nombres para el mismo concepto, solo difieren en el autor que las propone",
          "La objetiva es propia de Europa; la constructivista es exclusivamente latinoamericana"
        ],
        ans: 1,
        exp: "La concepción objetiva define la nación por rasgos empíricos: lengua, territorio, etnia, religión. La constructivista (Gellner, Anderson, Hobsbawm) sostiene que la nación es una construcción histórica moderna, ligada al capitalismo y al Estado moderno del siglo XIX, no algo natural ni eterno."
      },
      {
        q: "El pueblo kurdo es un ejemplo de:",
        opts: [
          "Nación que coincide plenamente con un Estado-nación",
          "Nación sin Estado propio",
          "Estado sin nación definida",
          "Nación plurinacional con múltiples Estados"
        ],
        ans: 1,
        exp: "Los kurdos tienen una identidad nacional clara (lengua, cultura, historia compartida) pero no tienen Estado propio: están divididos entre Turquía, Irak, Siria e Irán. Es el ejemplo clásico de nación sin Estado."
      }
    ]
  },
  sociedad: {
    name: "MÓDULO 3 — SOCIEDAD Y CIUDADANÍA",
    color: "#a088f0",
    questions: [
      {
        q: "¿Cuál de estos es un ejemplo de 'acción racional con arreglo a fines' según Weber?",
        opts: [
          "Un manifestante que protesta por la justicia aunque sepa que no logrará nada concreto",
          "Un empresario que calcula costos y beneficios para maximizar sus ganancias",
          "Una persona que vota por el mismo partido que votaba su familia hace décadas",
          "Un soldado que actúa impulsado por la furia ante el enemigo"
        ],
        ans: 1,
        exp: "La acción racional con arreglo a fines implica cálculo racional de medios y fines para lograr un objetivo específico. El empresario que calcula es el ejemplo clásico. Para Weber, es la forma de acción más característica del capitalismo moderno."
      },
      {
        q: "¿Qué distingue a la acción social de una conducta cualquiera según Weber?",
        opts: [
          "Que sea realizada por un grupo numeroso de personas",
          "Que sea una conducta con sentido para quien la realiza y orientada hacia otros",
          "Que tenga consecuencias políticas o económicas visibles",
          "Que sea deliberada y planificada con antelación"
        ],
        ans: 1,
        exp: "Para Weber, la acción social tiene dos elementos: tiene sentido subjetivo para quien la realiza, y está orientada hacia la conducta de otros. Un tropezón accidental no es acción social; una protesta organizada sí lo es."
      },
      {
        q: "Según Bourdieu, ¿qué tipos de capital determinan la posición social de una persona?",
        opts: [
          "Solo el capital económico (dinero y propiedades)",
          "Capital económico, cultural y social",
          "Capital político, militar y religioso",
          "Capital natural, heredado y adquirido"
        ],
        ans: 1,
        exp: "Bourdieu amplió el concepto de capital más allá de lo económico: el capital cultural (títulos, conocimientos, hábitos), el capital social (redes de contactos), y el económico. La combinación de estos tres determina la posición en el campo social."
      },
      {
        q: "¿Qué demostró el Cordobazo de 1969 respecto de la acción social?",
        opts: [
          "Que los trabajadores y estudiantes tenían intereses incompatibles",
          "Que la acción colectiva puede cambiar el rumbo político incluso bajo una dictadura",
          "Que la violencia política siempre fracasa ante el poder estatal",
          "Que Onganía tenía una legitimidad sólida para gobernar"
        ],
        ans: 1,
        exp: "El Cordobazo fue la acción conjunta del movimiento obrero y estudiantil contra la dictadura de Onganía. Su impacto fue tan grande que marcó el primer crack del régimen militar y demostró que la acción colectiva puede cambiar el rumbo político incluso bajo un gobierno autoritario."
      },
      {
        q: "¿Cuál es la función central de la sociedad civil?",
        opts: [
          "Reemplazar al Estado en la provisión de servicios públicos",
          "Limitar y controlar el poder estatal desde fuera del Estado",
          "Canalizar las demandas de los ciudadanos hacia el mercado económico",
          "Garantizar la gobernabilidad apoyando siempre las decisiones del gobierno"
        ],
        ans: 1,
        exp: "La sociedad civil es el espacio de organización ciudadana fuera del Estado. Incluye sindicatos, ONGs, iglesias, medios de comunicación. Su función central es limitar y controlar el poder estatal, actuando como contrapeso al gobierno."
      },
      {
        q: "La 'ciudadanía' se define mejor como:",
        opts: [
          "El documento de identidad que otorga el Estado a sus habitantes",
          "Un proceso histórico de expansión y disputa del 'derecho a tener derechos'",
          "La nacionalidad de una persona según su lugar de nacimiento",
          "El conjunto de obligaciones que tiene el individuo frente al Estado"
        ],
        ans: 1,
        exp: "La ciudadanía no es solo un estatus legal: es un proceso histórico de lucha y expansión. La expresión 'el derecho a tener derechos' (Hannah Arendt) captura su esencia: no es algo dado, sino algo que se conquista y que va cambiando con el tiempo."
      }
    ]
  },
  regimenes: {
    name: "MÓDULO 4 — REGÍMENES Y DEMOCRACIA",
    color: "#4a9eff",
    questions: [
      {
        q: "¿Cuál de estos NO es uno de los 6 atributos de la Poliarquía según Dahl?",
        opts: [
          "Sufragio universal, igual y secreto",
          "Igualdad económica garantizada por el Estado",
          "Libertad de expresión e información diversa",
          "Alternancia real entre partidos"
        ],
        ans: 1,
        exp: "La poliarquía es una definición MÍNIMA y PROCEDIMENTAL de democracia. No requiere igualdad económica o social. Los 6 atributos son procedimentales: sufragio universal, elecciones limpias, ejercicio del poder sin condicionamientos, alternancia real, pluralidad electoral y libertad de expresión."
      },
      {
        q: "¿Qué diferencia existe entre una 'transición de gobierno' y una 'transición de régimen'?",
        opts: [
          "Son lo mismo: ambas implican un cambio en las autoridades del Estado",
          "La transición de gobierno cambia quién gobierna dentro del mismo régimen; la de régimen cambia las reglas del juego",
          "La transición de régimen solo ocurre cuando hay un golpe de Estado violento",
          "La transición de gobierno es más importante porque afecta directamente a la ciudadanía"
        ],
        ans: 1,
        exp: "Una transición de gobierno es el cambio de quién gobierna (ej.: de un partido a otro en elecciones) dentro del mismo régimen democrático o autoritario. Una transición de régimen es un cambio profundo: de dictadura a democracia o viceversa. La segunda es mucho más trascendente."
      },
      {
        q: "¿Cuál es el rasgo más característico del populismo según la definición politológica?",
        opts: [
          "La implementación de políticas económicas redistributivas hacia los sectores populares",
          "La construcción de una división entre 'el pueblo' vs. 'la élite corrupta' encarnada en un líder",
          "La movilización de las clases trabajadoras en contra del capitalismo",
          "El uso de elecciones fraudulentas para mantenerse en el poder indefinidamente"
        ],
        ans: 1,
        exp: "El populismo se define por la construcción discursiva del 'pueblo' como sujeto puro y virtuoso frente a una 'élite corrupta' que lo oprime. El líder populista se presenta como la encarnación de la voluntad del pueblo. Puede ser de izquierda o de derecha."
      },
      {
        q: "Un sistema donde las unidades independientes se unen voluntariamente para formar un Estado federal se llama:",
        opts: [
          "Holding together",
          "Putting together",
          "Coming together",
          "Getting together"
        ],
        ans: 2,
        exp: "El modelo 'coming together' (unirse) es cuando unidades previamente independientes se federan voluntariamente, como los estados de EEUU. El 'holding together' es cuando un Estado unitario se descentraliza para mantener la unidad (España, India). El 'putting together' es la imposición del centro (URSS)."
      },
      {
        q: "¿Cuándo se considera que una democracia está 'consolidada' según la ciencia política?",
        opts: [
          "Cuando lleva más de 10 años consecutivos de gobierno democrático",
          "Cuando los principales actores políticos aceptan la democracia como el único juego posible",
          "Cuando el país alcanza un nivel de desarrollo económico alto",
          "Cuando desaparece completamente la posibilidad de un golpe de Estado"
        ],
        ans: 1,
        exp: "La consolidación democrática no es solo tiempo: es cuando los actores clave (militares, empresarios, partidos, sociedad civil) internalizan la democracia como la única forma legítima de acceso y ejercicio del poder, descartando las alternativas autoritarias."
      },
      {
        q: "¿Por qué los golpes militares disminuyeron en América Latina a partir de los años 90?",
        opts: [
          "Porque los ejércitos latinoamericanos fueron desmantelados tras los procesos de paz",
          "Por el descrédito militar post-dictaduras, la presión internacional de DDHH y la consolidación de normas democráticas",
          "Porque la prosperidad económica de los 90 eliminó los conflictos sociales",
          "Porque los EEUU prohibió los golpes militares mediante tratados internacionales"
        ],
        ans: 1,
        exp: "El declive de los golpes militares en AL se explica por: el descrédito de las FF.AA. tras dictaduras fracasadas (económicamente y como en Malvinas), la presión internacional y de organismos de DDHH, la consolidación de normas democráticas regionales y el surgimiento de nuevas formas de inestabilidad sin golpe directo."
      }
    ]
  },
  violencia: {
    name: "MÓDULO 5 — GOLPES, TERROR Y GENOCIDIO",
    color: "#f06060",
    questions: [
      {
        q: "¿Por qué el derrocamiento de Frondizi en 1962 se considera una 'interrupción institucional' y no un golpe de Estado?",
        opts: [
          "Porque Frondizi renunció voluntariamente sin presión militar",
          "Porque aunque los militares lo presionaron, asumió el titular del Senado (Guido) por acefalía, sin cambio de régimen",
          "Porque las Fuerzas Armadas garantizaron la continuidad constitucional en todo momento",
          "Porque el Congreso votó la destitución de Frondizi siguiendo el procedimiento constitucional"
        ],
        ans: 1,
        exp: "Aunque los militares presionaron a Frondizi para que renunciara, lo que ocurrió fue que asumió el Dr. José María Guido (presidente provisional del Senado) siguiendo la Ley de Acefalía. No hubo cambio de régimen democrático. Es el ejemplo favorito del examen para distinguir golpe de interrupción institucional."
      },
      {
        q: "¿Qué distingue al terrorismo de Estado del terrorismo 'convencional'?",
        opts: [
          "El terrorismo de Estado es menos violento porque está regulado por leyes",
          "El terrorismo de Estado usa recursos y aparato estatal para eliminar opositores y generar miedo masivo, violando el Estado de derecho que dice proteger",
          "El terrorismo de Estado solo se da en dictaduras, nunca en democracias",
          "El terrorismo de Estado tiene objetivos económicos mientras que el convencional tiene objetivos políticos"
        ],
        ans: 1,
        exp: "El terrorismo de Estado es ejercido por el propio Estado o con su amparo. Usa recursos estatales (fuerzas de seguridad, financiamiento, centros clandestinos) para eliminar opositores y aterrorizar a la sociedad. La paradoja es que viola el Estado de derecho que dice defender."
      },
      {
        q: "¿Cuál es el 'dolus specialis' en la definición jurídica de genocidio?",
        opts: [
          "El número mínimo de víctimas necesario para que un crimen sea considerado genocidio",
          "La intención específica de destruir total o parcialmente a un grupo como tal",
          "La planificación previa y sistemática del exterminio por parte del Estado",
          "La participación de agentes estatales en la comisión del crimen"
        ],
        ans: 1,
        exp: "El dolus specialis (dolo especial) es el elemento mental que define al genocidio: la conducta debe tener como objetivo específico destruir total o parcialmente a un grupo nacional, étnico, racial o religioso 'como tal'. Sin esta intención específica, puede ser crimen de lesa humanidad pero no genocidio."
      },
      {
        q: "¿Qué grupos quedaron EXCLUIDOS de la protección de la Convención del Genocidio de 1948?",
        opts: [
          "Los grupos étnicos y raciales, considerados demasiado amplios para definir",
          "Los grupos políticos y sociales",
          "Los grupos religiosos, por el principio de separación Iglesia-Estado",
          "Los grupos nacionales de países que no firmaron la Convención"
        ],
        ans: 1,
        exp: "La Convención de 1948 protege grupos nacionales, étnicos, raciales y religiosos. Los grupos políticos y sociales quedaron EXCLUIDOS, principalmente por presión de la URSS, que temía que sus purgas políticas fueran calificadas como genocidio. Esto genera el debate sobre si la dictadura argentina cometió genocidio."
      },
      {
        q: "En las '4 olas del terrorismo' de Rapoport, ¿en cuál se enmarca principalmente la violencia política argentina de los años 70?",
        opts: [
          "Primera ola: anarquista (fines del siglo XIX)",
          "Segunda ola: anticolonial (post Segunda Guerra Mundial)",
          "Tercera ola: nueva izquierda (décadas de 1960-70)",
          "Cuarta ola: religiosa (desde los años 80)"
        ],
        ans: 2,
        exp: "La violencia política argentina de los años 70 (Montoneros, ERP) se enmarca en la tercera ola de Rapoport: la de la 'nueva izquierda', caracterizada por grupos guerrilleros de inspiración marxista, maoísta o foquista que operaron en los países occidentales y latinoamericanos durante los años 60 y 70."
      },
      {
        q: "¿Qué es un 'autogolpe' y cuál es el ejemplo más citado en la bibliografía?",
        opts: [
          "Cuando el ejército se divide y se golpea internamente; ejemplo: Argentina en 1987",
          "Cuando el propio gobernante rompe el orden constitucional para concentrar poder; ejemplo: Fujimori en Perú (1992)",
          "Cuando un gobierno extranjero financia un golpe interno; ejemplo: Chile en 1973",
          "Cuando el poder legislativo destituye al ejecutivo; ejemplo: Brasil en 2016"
        ],
        ans: 1,
        exp: "El autogolpe (o 'fujimorazo') ocurre cuando el propio gobernante, en lugar de ser derrocado, es quien viola el orden constitucional para concentrar poder y gobernar sin controles. Fujimori en Perú en 1992 es el ejemplo paradigmático en la bibliografía."
      }
    ]
  },
  argentina: {
    name: "MÓDULO 6 — ARGENTINA 1966–1983",
    color: "#f07060",
    questions: [
      {
        q: "¿Por qué el golpe de 1966 (Onganía) se considera diferente a los golpes anteriores de 1930, 1943 y 1955?",
        opts: [
          "Porque fue el primero en contar con apoyo popular masivo",
          "Porque fue el primer golpe con intención de permanencia: no buscaba ser transitorio sino instaurar un proyecto de largo plazo",
          "Porque fue el primero en usar la represión física sistemática contra la población",
          "Porque fue el único golpe que contó con apoyo de partidos políticos de izquierda"
        ],
        ans: 1,
        exp: "Los golpes anteriores (1930, 1943, 1955) tenían carácter transitorio: los militares buscaban restaurar el orden y llamar a elecciones. La Revolución Argentina de 1966 fue el primero con vocación de permanencia: tenía un proyecto de modernización autoritaria de largo plazo. Esto lo hace cualitativamente diferente."
      },
      {
        q: "¿Qué fue el 'Cordobazo' y qué demostró?",
        opts: [
          "Una operación militar para reprimir la guerrilla en Córdoba en 1969",
          "Una revuelta obrero-estudiantil en 1969 que demostró la capacidad de la acción colectiva para desestabilizar una dictadura",
          "El golpe de Estado que derrocó a Onganía en Córdoba",
          "El primer atentado de Montoneros contra instalaciones militares en Córdoba"
        ],
        ans: 1,
        exp: "El Cordobazo (mayo 1969) fue la unión del movimiento obrero y estudiantil en una revuelta que sacudió a la dictadura de Onganía. Demostró que la acción colectiva puede cambiar el rumbo político y fue el primer crack serio del régimen. Aceleró la caída de Onganía."
      },
      {
        q: "¿Qué fue la 'tablita cambiaria' y cuál fue su consecuencia?",
        opts: [
          "Un plan de congelamiento de precios que controló la inflación durante el Proceso",
          "Un tipo de cambio preanunciado que sobrevaluó el peso, facilitando la importación, el endeudamiento y la especulación financiera",
          "La reforma tributaria de Martínez de Hoz que gravó las importaciones para proteger la industria",
          "El acuerdo de precios entre el gobierno militar y las grandes empresas"
        ],
        ans: 1,
        exp: "La 'tablita' era el tipo de cambio preanunciado de Martínez de Hoz que hacía barato el dólar y los productos importados. Esto generó la 'plata dulce' (consumo importado) y la 'bicicleta financiera' (especulación). El resultado fue desindustrialización, endeudamiento externo masivo y la crisis financiera de 1980-82."
      },
      {
        q: "¿Por qué el 'verdadero objetivo' del terrorismo de Estado según Romero eran 'los vivos' y no los desaparecidos?",
        opts: [
          "Porque el objetivo era eliminar físicamente a toda la oposición política viva en Argentina",
          "Porque la desaparición (sin cuerpo, sin certeza) maximizaba el efecto intimidatorio sobre la sociedad en su conjunto para disciplinarla y silenciarla",
          "Porque el régimen quería que la sociedad colaborara en la identificación de subversivos",
          "Porque el terror tenía como objetivo principal el control económico de la clase media"
        ],
        ans: 1,
        exp: "El terrorismo de Estado no buscaba solo eliminar opositores: buscaba generar terror masivo en toda la sociedad para paralizarla y disciplinarla. La desaparición era más efectiva que la muerte: sin cuerpo, sin certeza del destino, el miedo se expandía a familia, vecinos, compañeros. El mensaje iba dirigido a todos."
      },
      {
        q: "¿Por qué la derrota en Malvinas aceleró el fin de la dictadura?",
        opts: [
          "Porque la comunidad internacional impuso sanciones económicas que colapsaron la economía",
          "Porque la derrota deslegitimó definitivamente a las FF.AA., eliminó su capacidad de imponer condiciones a la transición y desintegró el régimen",
          "Porque el ejército perdió el apoyo de los Estados Unidos que era su principal sostén",
          "Porque los soldados combatientes se rebelaron al regresar y exigieron democracia"
        ],
        ans: 1,
        exp: "Galtieri buscó apoyo popular con Malvinas para salir de la crisis interna. La derrota completa tuvo el efecto contrario: deslegitimó totalmente a las FF.AA. como institución rectora, generó fracturas internas, eliminó su capacidad de negociar la salida y aceleró la transición sin condiciones para los militares."
      },
      {
        q: "¿Cuál fue la principal característica del clima político previo al golpe del 24 de marzo de 1976?",
        opts: [
          "Alta estabilidad económica y baja conflictividad social",
          "Alta violencia política, crisis económica aguda, debilidad del gobierno de Isabel y polarización extrema con 'lógica de enfrentamiento'",
          "Gobierno fuerte de Isabel que no podía ser derrocado por la presión popular",
          "Consenso social amplio para una reforma constitucional pacífica"
        ],
        ans: 1,
        exp: "El clima pre-76 se caracterizó por: alta violencia política (Montoneros, ERP, Triple A), crisis económica aguda, muerte de Perón y debilidad de Isabel, y polarización social con una 'lógica de enfrentamiento'. Este contexto hizo que sectores civiles vieran el golpe como una 'solución', lo que facilitó su instalación."
      }
    ]
  },
  transicion: {
    name: "MÓDULO 7 — TRANSICIÓN Y DDHH",
    color: "#3fcf8e",
    questions: [
      {
        q: "¿Por qué la transición democrática de 1983 fue más exitosa que la de 1973?",
        opts: [
          "Porque en 1983 había más partidos políticos y mayor pluralismo ideológico",
          "Porque la derrota de Malvinas deslegitimó a los militares y la sociedad había madurado convergiendo en la democracia como valor transversal",
          "Porque en 1973 no hubo elecciones libres, mientras que en 1983 sí",
          "Porque en 1983 los partidos peronista y radical acordaron previamente las reglas de la transición"
        ],
        ans: 1,
        exp: "En 1973 había polarización extrema y 'lógica de enfrentamiento'. En 1983, la derrota de Malvinas deslegitimó completamente a los militares (sin poder de veto), y la sociedad había madurado: la democracia era un valor transversal que unía a distintos sectores más allá de los partidos."
      },
      {
        q: "¿Por qué el Juicio a las Juntas de 1985 fue un hito histórico mundial?",
        opts: [
          "Porque fue el primer juicio internacional a un gobierno latinoamericano por crímenes de guerra",
          "Porque fue el primer caso en que una democracia juzgó a sus propios ex dictadores en sus propios tribunales",
          "Porque se aplicó por primera vez la figura jurídica de genocidio a los crímenes de la dictadura",
          "Porque las sentencias incluyeron la restitución de bienes a todas las familias de los desaparecidos"
        ],
        ans: 1,
        exp: "El Juicio a las Juntas fue históricamente significativo porque Argentina se convirtió en el primer país en juzgar a sus propios dictadores en democracia, usando sus propios tribunales civiles. Mostró que la democracia podía hacer justicia sin venganza ni impunidad, y sentó un precedente mundial."
      },
      {
        q: "¿Por qué Alfonsín sancionó las leyes de Punto Final y Obediencia Debida?",
        opts: [
          "Porque ideológicamente estaba de acuerdo con perdonar a los militares",
          "Por la presión de los levantamientos 'carapintadas' de 1987-88, con el argumento de preservar la democracia frente a la amenaza de un nuevo golpe",
          "Porque los organismos de DDHH le solicitaron que pusiera un límite a los juicios para no desestabilizar el país",
          "Porque la Corte Suprema declaró inconstitucionales los juicios militares"
        ],
        ans: 1,
        exp: "Alfonsín cedió ante los levantamientos militares 'carapintadas' (Semana Santa 1987, Monte Caseros 1988). La Ley de Punto Final limitó temporalmente los nuevos juicios y la Ley de Obediencia Debida eximió a quienes 'cumplían órdenes'. Fueron muy cuestionadas por organismos de DDHH y luego anuladas en 2003."
      },
      {
        q: "¿Cuál es la base filosófica kantiana de los Derechos Humanos?",
        opts: [
          "Que los derechos nacen del contrato social y pueden ser modificados por la mayoría democrática",
          "Que el ser humano es un fin en sí mismo y nunca debe ser usado como medio: tiene dignidad inherente por su racionalidad",
          "Que los derechos son concesiones del Estado que puede recuperar si el ciudadano viola sus obligaciones",
          "Que los derechos humanos son universales porque derivan de la naturaleza biológica compartida de la especie"
        ],
        ans: 1,
        exp: "Kant sostuvo que cada ser humano tiene dignidad inherente porque es un ser racional y libre: debe ser tratado como fin en sí mismo, NUNCA como mero instrumento para los fines de otro. Esta idea fundamenta que los DDHH no pueden ser negados por ningún Estado, porque nacen de la condición humana misma."
      },
      {
        q: "¿Qué significa que los crímenes de lesa humanidad sean 'imprescriptibles'?",
        opts: [
          "Que no pueden ser juzgados después de 10 años de ocurridos",
          "Que no existe plazo para juzgarlos: pueden procesarse aunque hayan pasado décadas",
          "Que solo pueden juzgarse en los países donde ocurrieron los crímenes",
          "Que requieren una declaración especial de la ONU para ser investigados"
        ],
        ans: 1,
        exp: "La imprescriptibilidad significa que los crímenes de lesa humanidad (genocidio, tortura sistemática, desaparición forzada como parte de un plan estatal) no tienen plazo de prescripción: pueden juzgarse aunque hayan pasado décadas. También pueden juzgarse internacionalmente (jurisdicción universal). Esto fue fundamental para los juicios argentinos post-2003."
      },
      {
        q: "¿Cuáles son los tres deberes del Estado respecto de los Derechos Humanos según el Capítulo 14 (Montero)?",
        opts: [
          "Declarar, publicitar y financiar los derechos humanos",
          "Respetar (no interferir), proteger (evitar abusos de terceros) y promover (garantizar acceso a derechos)",
          "Legislar, ejecutar y juzgar los derechos humanos",
          "Universalizar, inalienar e indivisibilizar los derechos humanos"
        ],
        ans: 1,
        exp: "Montero identifica tres deberes estatales respecto de los DDHH: (1) Respetar: no interferir directamente con los derechos (no torturar, no censurar); (2) Proteger: impedir que terceros violen derechos; (3) Promover: crear condiciones para que todos puedan ejercerlos mediante políticas públicas."
      }
    ]
  }
};

// =============================================
// QUIZ ENGINE
// =============================================
let currentModule = null;
let queue = [];
let reviewQueue = [];
let currentQIndex = 0;
let sessionStats = {};
let totalCorrect = 0, totalWrong = 0, streak = 0, totalAnswered = 0;
let questionRecord = [];
let reviewTimers = {};
let countdownTimer = null;
let answered = false;

function initSessionStats() {
  totalCorrect = 0; totalWrong = 0; streak = 0; totalAnswered = 0;
  questionRecord = [];
  reviewQueue = [];
  Object.keys(reviewTimers).forEach(t => clearTimeout(reviewTimers[t]));
  reviewTimers = {};
}

function getWrongCount(qIndex) {
  return questionRecord.filter(r => r.index === qIndex && !r.correct).length;
}

function calcReviewDelay(wrongCountInSession, totalWrong) {
  // If only 1 wrong question total: no wait
  // Scale: the more wrong answers, the longer the delay (max 60s)
  if (totalWrong <= 1) return 0;
  const ratio = Math.min(wrongCountInSession / 3, 1);
  return Math.round(ratio * 60);
}

function shuffleArray(arr) {
  const a = [...arr];
  for (let i = a.length - 1; i > 0; i--) {
    const j = Math.floor(Math.random() * (i + 1));
    [a[i], a[j]] = [a[j], a[i]];
  }
  return a;
}

function openQuiz(moduleId) {
  currentModule = moduleId;
  initSessionStats();
  const data = QUIZ_DATA[moduleId];
  queue = shuffleArray(data.questions.map((q, i) => ({ ...q, origIndex: i })));
  currentQIndex = 0;

  document.getElementById('quizModuleName').textContent = data.name;
  document.getElementById('quizOverlay').classList.add('active');
  document.getElementById('quizMainView').style.display = '';
  document.getElementById('quizResults').classList.remove('active');
  document.body.style.overflow = 'hidden';

  renderQuestion();
  updateScorebar();
}

function closeQuiz() {
  document.getElementById('quizOverlay').classList.remove('active');
  document.body.style.overflow = '';
  Object.keys(reviewTimers).forEach(t => clearTimeout(reviewTimers[t]));
  if (countdownTimer) clearInterval(countdownTimer);
  updateMiniStats(currentModule);
}

function renderQuestion() {
  if (currentQIndex >= queue.length) {
    if (reviewQueue.length > 0) {
      const next = reviewQueue.shift();
      queue.push(next);
    } else {
      showResults();
      return;
    }
  }

  const qData = queue[currentQIndex];
  answered = false;

  // progress
  const totalQ = QUIZ_DATA[currentModule].questions.length;
  const seen = Math.min(totalAnswered, totalQ);
  document.getElementById('quizProgressBar').style.width = (seen / totalQ * 100) + '%';
  document.getElementById('quizProgressText').textContent = seen + '/' + totalQ;

  // badges
  const badgeRow = document.getElementById('quizBadgeRow');
  const wc = getWrongCount(qData.origIndex);
  let badges = '';
  if (wc > 0) badges += `<span class="q-badge review">↺ REPASO #${wc+1}</span>`;
  else badges += `<span class="q-badge new">NUEVA</span>`;
  const diff = wc === 0 ? 'Normal' : wc === 1 ? 'Difícil' : 'Muy difícil';
  badges += `<span class="q-badge difficulty">${diff}</span>`;
  badgeRow.innerHTML = badges;

  // shuffle options
  const opts = qData.opts;
  const correctText = opts[qData.ans];
  const shuffledOpts = shuffleArray(opts.map((o, i) => ({ text: o, isCorrect: i === qData.ans })));

  document.getElementById('quizQuestionText').textContent = qData.q;

  const optsEl = document.getElementById('quizOptions');
  const letters = ['A', 'B', 'C', 'D'];
  optsEl.innerHTML = shuffledOpts.map((o, i) => `
    <button class="quiz-option" onclick="selectOption(this, ${o.isCorrect}, '${escHtml(o.text)}', '${escHtml(correctText)}')" data-correct="${o.isCorrect}">
      <span class="opt-letter">${letters[i]}.</span>
      <span>${o.text}</span>
    </button>
  `).join('');

  document.getElementById('quizFeedback').style.display = 'none';
  document.getElementById('quizNextBtn').classList.remove('visible');
  document.getElementById('reviewCountdown').classList.remove('visible');
  if (countdownTimer) clearInterval(countdownTimer);

  // animate card
  const card = document.getElementById('quizCard');
  card.style.animation = 'none';
  card.offsetHeight;
  card.style.animation = 'slideIn 0.25s ease';
}

function escHtml(s) { return s.replace(/'/g, "\\'"); }

function selectOption(btn, isCorrect, selectedText, correctText) {
  if (answered) return;
  answered = true;
  const qData = queue[currentQIndex];

  // Disable all options
  document.querySelectorAll('.quiz-option').forEach(b => b.classList.add('disabled'));

  if (isCorrect) {
    btn.classList.add('correct-pick');
    totalCorrect++;
    streak++;
    questionRecord.push({ index: qData.origIndex, correct: true, q: qData.q });
  } else {
    btn.classList.add('wrong-pick');
    totalWrong++;
    streak = 0;
    questionRecord.push({ index: qData.origIndex, correct: false, q: qData.q });
    // Highlight correct
    document.querySelectorAll('.quiz-option').forEach(b => {
      if (b.dataset.correct === 'true') b.classList.add('correct-answer');
    });
  }
  totalAnswered++;
  updateScorebar();

  // Show feedback
  const fb = document.getElementById('quizFeedback');
  fb.className = 'quiz-feedback ' + (isCorrect ? 'correct' : 'wrong');
  fb.innerHTML = `<span class="fb-label">${isCorrect ? '✓ ¡Correcto!' : '✗ Incorrecto'}</span><span class="fb-explanation">${qData.exp}</span>`;
  fb.style.display = 'block';

  if (!isCorrect) {
    // Calculate review delay
    const wrongInSession = questionRecord.filter(r => r.index === qData.origIndex && !r.correct).length;
    const delay = calcReviewDelay(wrongInSession, totalWrong);

    if (delay <= 0) {
      // No wait: push directly to review queue
      reviewQueue.push({ ...qData });
      document.getElementById('quizNextBtn').textContent = 'Siguiente →';
      document.getElementById('quizNextBtn').classList.add('visible');
    } else {
      // Show countdown
      const countdown = document.getElementById('reviewCountdown');
      const countdownLabel = document.getElementById('countdownLabel');
      const countdownSecs = document.getElementById('countdownSecs');
      const countdownBar = document.getElementById('countdownBar');

      countdown.classList.add('visible');
      countdownLabel.textContent = 'Esta pregunta vuelve en:';
      countdownSecs.textContent = delay + 's';
      countdownBar.style.width = '100%';

      let remaining = delay;
      const start = Date.now();

      countdownTimer = setInterval(() => {
        remaining = delay - Math.floor((Date.now() - start) / 1000);
        if (remaining <= 0) {
          clearInterval(countdownTimer);
          countdown.classList.remove('visible');
          reviewQueue.push({ ...qData });
          document.getElementById('quizNextBtn').textContent = 'Siguiente →';
          document.getElementById('quizNextBtn').classList.add('visible');
        } else {
          countdownSecs.textContent = remaining + 's';
          countdownBar.style.width = (remaining / delay * 100) + '%';
        }
      }, 200);

      // Also show next button immediately but disabled-looking until timer
      document.getElementById('quizNextBtn').textContent = `Esperá ${delay}s... →`;
      document.getElementById('quizNextBtn').classList.add('visible');
      document.getElementById('quizNextBtn').style.opacity = '0.4';
      document.getElementById('quizNextBtn').style.pointerEvents = 'none';

      const restoreBtn = () => {
        document.getElementById('quizNextBtn').style.opacity = '';
        document.getElementById('quizNextBtn').style.pointerEvents = '';
        document.getElementById('quizNextBtn').textContent = 'Siguiente →';
      };
      reviewTimers['btn_' + Date.now()] = setTimeout(restoreBtn, delay * 1000);
    }
  } else {
    document.getElementById('quizNextBtn').textContent = 'Siguiente →';
    document.getElementById('quizNextBtn').classList.add('visible');
  }
}

function nextQuestion() {
  currentQIndex++;
  renderQuestion();
}

function updateScorebar() {
  document.getElementById('chipCorrect').textContent = `✓ ${totalCorrect} correcta${totalCorrect !== 1 ? 's' : ''}`;
  document.getElementById('chipWrong').textContent = `✗ ${totalWrong} error${totalWrong !== 1 ? 'es' : ''}`;
  document.getElementById('chipStreak').textContent = `🔥 racha: ${streak}`;
  document.getElementById('chipTotal').textContent = `respondidas: ${totalAnswered}`;
}

// =============================================
// RESULTS
// =============================================
function showResults() {
  document.getElementById('quizMainView').style.display = 'none';
  const resultsEl = document.getElementById('quizResults');
  resultsEl.classList.add('active');

  const totalQ = QUIZ_DATA[currentModule].questions.length;
  const pct = totalAnswered > 0 ? Math.round((totalCorrect / totalAnswered) * 100) : 0;
  const uniqueCorrect = [...new Set(
    questionRecord.filter(r => r.correct).map(r => r.index)
  )].length;

  // Grade
  let grade, gradeColor, subtitle;
  if (pct >= 90) { grade = '★ A'; gradeColor = '#3fcf8e'; subtitle = '¡Excelente! Dominás el módulo.'; }
  else if (pct >= 70) { grade = 'B'; gradeColor = '#4a9eff'; subtitle = 'Muy bien. Repasá los errores.'; }
  else if (pct >= 50) { grade = 'C'; gradeColor = '#f0a030'; subtitle = 'Aprobado justo. A repasar.'; }
  else { grade = 'D'; gradeColor = '#f06060'; subtitle = 'Necesitás repasar este módulo completo.'; }

  document.getElementById('resultsGrade').textContent = grade;
  document.getElementById('resultsGrade').style.color = gradeColor;
  document.getElementById('resultsSubtitle').textContent = subtitle;

  // Grid
  const maxStreak = (() => {
    let max = 0, cur = 0;
    questionRecord.forEach(r => { if (r.correct) { cur++; max = Math.max(max, cur); } else cur = 0; });
    return max;
  })();

  document.getElementById('resultsGrid').innerHTML = `
    <div class="res-chip c"><div class="res-chip-val">${uniqueCorrect}/${totalQ}</div><div class="res-chip-label">Correctas únicas</div></div>
    <div class="res-chip w"><div class="res-chip-val">${totalWrong}</div><div class="res-chip-label">Total de errores</div></div>
    <div class="res-chip s"><div class="res-chip-val">${maxStreak}</div><div class="res-chip-label">Racha máxima</div></div>
    <div class="res-chip"><div class="res-chip-val" style="color:var(--amber)">${pct}%</div><div class="res-chip-label">Precisión</div></div>
  `;

  // Wrong questions
  const wrongItems = QUIZ_DATA[currentModule].questions.map((q, i) => {
    const wrongs = questionRecord.filter(r => r.index === i && !r.correct).length;
    const rights = questionRecord.filter(r => r.index === i && r.correct).length;
    return { q: q.q, wrongs, rights, index: i };
  }).filter(x => x.wrongs > 0).sort((a, b) => b.wrongs - a.wrongs);

  const correctItems = QUIZ_DATA[currentModule].questions.map((q, i) => {
    const wrongs = questionRecord.filter(r => r.index === i && !r.correct).length;
    const rights = questionRecord.filter(r => r.index === i && r.correct).length;
    return { q: q.q, wrongs, rights };
  }).filter(x => x.wrongs === 0 && x.rights > 0);

  let wrongHTML = '';
  if (wrongItems.length > 0) {
    wrongHTML = `<div class="results-section-title">✗ Preguntas con errores (${wrongItems.length})</div>`;
    wrongItems.forEach(item => {
      const repText = item.wrongs === 1 ? 'fallaste 1 vez — repasar en 1 día' :
                      item.wrongs === 2 ? 'fallaste 2 veces — repasar hoy' :
                      `fallaste ${item.wrongs} veces — repasar ahora`;
      wrongHTML += `<div class="results-q-item wrong">
        <div class="rq-q">${item.q}</div>
        <div class="rq-meta">
          <span class="rq-times">✗ ${item.wrongs} error${item.wrongs !== 1 ? 'es' : ''}</span>
          <span class="rq-next">${repText}</span>
        </div>
      </div>`;
    });
  }
  document.getElementById('resultsWrongList').innerHTML = wrongHTML;

  let correctHTML = '';
  if (correctItems.length > 0) {
    correctHTML = `<div class="results-section-title" style="margin-top:1rem">✓ Preguntas dominadas (${correctItems.length})</div>`;
    correctItems.forEach(item => {
      correctHTML += `<div class="results-q-item correct">
        <div class="rq-q">${item.q}</div>
        <div class="rq-meta"><span class="rq-ok">✓ Sin errores — repasar en 2 días</span></div>
      </div>`;
    });
  }
  document.getElementById('resultsCorrectList').innerHTML = correctHTML;

  // Suggestion
  let sug = '<div class="sug-title">📋 Plan de repaso sugerido</div>';
  if (wrongItems.length === 0) {
    sug += '<div class="sug-item">🎉 <strong>¡Perfecto!</strong> No tuviste errores. Revisá este módulo en 3 días.</div>';
  } else {
    wrongItems.slice(0, 3).forEach(item => {
      const freq = item.wrongs >= 3 ? 'HOY (repaso urgente)' : item.wrongs === 2 ? 'mañana' : 'en 2 días';
      sug += `<div class="sug-item">⚠ <strong>Repasar ${freq}:</strong> "${item.q.substring(0, 60)}..."</div>`;
    });
  }
  document.getElementById('resultsSuggestion').innerHTML = sug;

  // Save to localStorage-like in memory
  updateMiniStats(currentModule);
}

function restartQuiz() {
  openQuiz(currentModule);
}

// Mini stats display
const moduleMemory = {};
function updateMiniStats(moduleId) {
  const el = document.getElementById('stats-' + moduleId);
  if (!el) return;
  const correct = questionRecord.filter(r => r.correct).length;
  const wrong = questionRecord.filter(r => !r.correct).length;
  if (correct + wrong === 0) { el.innerHTML = ''; return; }
  el.innerHTML = `<span class="stat-correct">✓ ${correct}</span><span class="stat-wrong">✗ ${wrong}</span>`;
}

// =============================================
// ACCORDIONS
// =============================================
function buildAccordion(containerId, items) {
  const el = document.getElementById(containerId);
  if (!el) return;
  el.innerHTML = items.map((item, i) => `
    <div class="acc-item" id="${containerId}-${i}">
      <div class="acc-q" onclick="toggleAcc('${containerId}-${i}')">
        <span>${item.q}</span>
        <div class="acc-icon">+</div>
      </div>
      <div class="acc-a">
        <div class="acc-a-inner">${item.a}</div>
      </div>
    </div>`).join('');
}

function toggleAcc(id) {
  document.getElementById(id).classList.toggle('open');
}

buildAccordion('acc-estado', [
  {q: '¿Qué significa el "monopolio de la violencia legítima"? Dá un ejemplo.',
   a: 'Significa que solo el Estado puede usar la fuerza de manera legal y aceptada socialmente, a través de instituciones como la policía o el ejército. Por ejemplo, la policía puede detener a una persona porque actúa bajo normas legales. Si grupos armados ejercen violencia por fuera del control estatal, la autoridad del Estado se debilita.'},
  {q: '¿Por qué el Estado necesita legitimidad además de coerción?',
   a: 'La pura fuerza no alcanza para sostenerse en el tiempo. La población debe reconocer la autoridad como válida (legítima). Si el Estado solo usa la fuerza sin legitimidad, genera resistencia constante. Por eso Weber señala que el poder estatal se basa en la combinación de coerción (fuerza) y legitimidad (aceptación).'},
  {q: '¿Cuál es la diferencia entre Estado y gobierno?',
   a: 'El Estado es la estructura permanente: territorio, normas, instituciones, monopolio de la fuerza. El gobierno está formado por quienes administran el Estado temporalmente. Los gobiernos cambian con las elecciones o los golpes; el Estado continúa. Confundirlos es un error conceptual básico.'},
  {q: '¿Por qué la misma definición jurídica abarca al Estado liberal y al fascista?',
   a: 'Porque todos los tipos de Estado comparten los mismos elementos básicos: territorio, población, soberanía y sistema jurídico. Lo que varía es cómo los organizan: quién concentra el poder, qué derechos se garantizan, cómo funciona la economía. La definición de Weber es lo suficientemente abstracta para incluir modelos muy distintos.'},
  {q: 'Explicá los tres tipos de legitimidad de Weber.',
   a: '<strong>Tradicional:</strong> se basa en la costumbre y el hábito. Se obedece porque "siempre fue así". Ej.: monarquías hereditarias. <strong>Carismática:</strong> se basa en las cualidades personales extraordinarias de un líder. Sin ese líder, se desvanece. Ej.: Perón. <strong>Legal-racional:</strong> se fundamenta en normas y leyes racionalmente creadas. Se obedece a la ley, no a la persona. Es la base de los Estados modernos democráticos.'}
]);

buildAccordion('acc-nacion', [
  {q: '¿Por qué la nación es una construcción histórica y no algo natural?',
   a: 'Según Gellner, Anderson y Hobsbawm, la idea de nación surge en la modernidad (s. XIX) como construcción política ligada al Estado moderno, al capitalismo y a la imprenta. No es eterna ni natural. Las "tradiciones" nacionales muchas veces fueron inventadas para crear cohesión. Anderson la llama "comunidad imaginada".'},
  {q: '¿Qué herramientas usó el Estado argentino para construir la nación?',
   a: 'Educación pública (Ley 1420, escuela laica y gratuita), fiestas patrias, historia oficial que narraba un origen común, símbolos nacionales (bandera, himno), monumentos, servicio militar obligatorio. Todo en un contexto de alta inmigración masiva que hacía urgente crear una identidad compartida.'},
  {q: '¿Por qué en Argentina primero se formó el Estado y después la nación?',
   a: 'Porque las élites criollas construyeron las instituciones estatales después de la independencia (1810-1880) antes de que existiera una identidad nacional consolidada. La nación fue luego construida "desde arriba" mediante políticas públicas. En Europa, en cambio, generalmente la nación preexistía al Estado.'}
]);
</script>
</body>
</html>
