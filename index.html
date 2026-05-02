<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <meta name="theme-color" content="#6366f1">
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
    <title>FlashMind - Flashcards</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; -webkit-tap-highlight-color: transparent; }
        :root {
            --primary: #6366f1;
            --primary-dark: #4f46e5;
            --secondary: #8b5cf6;
            --accent: #ec4899;
            --bg: #f8fafc;
            --surface: #ffffff;
            --text: #1e293b;
            --text-secondary: #64748b;
            --border: #e2e8f0;
            --shadow: 0 4px 6px -1px rgba(0,0,0,0.1);
            --shadow-lg: 0 20px 25px -5px rgba(0,0,0,0.1);
        }
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            background: var(--bg);
            color: var(--text);
            height: 100vh;
            overflow: hidden;
            position: relative;
        }

        @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }
        @keyframes slideUp { from { transform: translateY(100%); } to { transform: translateY(0); } }

        .app-container {
            height: 100vh;
            display: flex;
            flex-direction: column;
            max-width: 480px;
            margin: 0 auto;
            background: var(--bg);
            position: relative;
            box-shadow: 0 0 40px rgba(0,0,0,0.1);
        }

        .header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 16px 20px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            z-index: 100;
            box-shadow: var(--shadow);
        }
        .header h1 { font-size: 1.25rem; font-weight: 700; display: flex; align-items: center; gap: 8px; }
        .header-icon { font-size: 1.5rem; }
        .header-actions { display: flex; gap: 12px; }
        .btn-icon {
            background: rgba(255,255,255,0.2);
            border: none;
            color: white;
            width: 36px;
            height: 36px;
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            font-size: 1.1rem;
            transition: all 0.2s;
        }
        .btn-icon:hover { background: rgba(255,255,255,0.3); transform: scale(1.1); }
        .btn-icon:active { transform: scale(0.95); }

        .search-container {
            padding: 12px 16px;
            background: var(--surface);
            border-bottom: 1px solid var(--border);
            animation: fadeIn 0.3s ease;
        }
        .search-box {
            display: flex;
            align-items: center;
            background: var(--bg);
            border-radius: 12px;
            padding: 10px 14px;
            gap: 10px;
            border: 2px solid transparent;
            transition: border-color 0.2s;
        }
        .search-box:focus-within { border-color: var(--primary); }
        .search-box input {
            flex: 1;
            border: none;
            background: none;
            font-size: 0.95rem;
            outline: none;
            color: var(--text);
        }
        .search-box input::placeholder { color: var(--text-secondary); }
        .search-clear {
            background: var(--text-secondary);
            color: white;
            border: none;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            font-size: 0.7rem;
            cursor: pointer;
            display: none;
        }
        .search-clear.visible { display: flex; align-items: center; justify-content: center; }

        .content {
            flex: 1;
            overflow-y: auto;
            padding: 16px;
            -webkit-overflow-scrolling: touch;
        }
        .content::-webkit-scrollbar { width: 0; }

        .empty-state {
            text-align: center;
            padding: 60px 20px;
            color: var(--text-secondary);
            animation: fadeIn 0.5s ease;
        }
        .empty-state .icon { font-size: 4rem; margin-bottom: 16px; opacity: 0.5; }
        .empty-state h3 { font-size: 1.1rem; margin-bottom: 8px; color: var(--text); }
        .empty-state p { font-size: 0.9rem; line-height: 1.5; }

        .folders-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 12px;
            animation: fadeIn 0.4s ease;
        }
        .folder-card {
            background: var(--surface);
            border-radius: 16px;
            padding: 16px;
            box-shadow: var(--shadow);
            cursor: pointer;
            transition: all 0.2s;
            position: relative;
            overflow: hidden;
            border: 2px solid transparent;
        }
        .folder-card:hover { transform: translateY(-2px); box-shadow: var(--shadow-lg); }
        .folder-card:active { transform: scale(0.98); }
        .folder-icon {
            width: 48px;
            height: 48px;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            margin-bottom: 10px;
        }
        .folder-name {
            font-weight: 600;
            font-size: 0.9rem;
            margin-bottom: 4px;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }
        .folder-count {
            font-size: 0.75rem;
            color: var(--text-secondary);
        }
        .folder-actions {
            position: absolute;
            top: 8px;
            right: 8px;
            display: flex;
            gap: 4px;
            opacity: 0;
            transition: opacity 0.2s;
        }
        .folder-card:hover .folder-actions { opacity: 1; }
        .folder-action-btn {
            background: var(--bg);
            border: none;
            width: 28px;
            height: 28px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 0.8rem;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .flashcards-list {
            display: flex;
            flex-direction: column;
            gap: 10px;
            animation: fadeIn 0.3s ease;
        }
        .flashcard-item {
            background: var(--surface);
            border-radius: 14px;
            padding: 14px 16px;
            box-shadow: var(--shadow);
            cursor: pointer;
            transition: all 0.2s;
            display: flex;
            align-items: center;
            gap: 12px;
            border: 2px solid transparent;
        }
        .flashcard-item:hover { border-color: var(--primary); }
        .flashcard-item:active { transform: scale(0.99); }
        .flashcard-preview {
            width: 50px;
            height: 50px;
            border-radius: 10px;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.3rem;
            flex-shrink: 0;
            color: white;
        }
        .flashcard-info { flex: 1; min-width: 0; }
        .flashcard-front {
            font-weight: 600;
            font-size: 0.9rem;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            margin-bottom: 4px;
        }
        .flashcard-back-preview {
            font-size: 0.8rem;
            color: var(--text-secondary);
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }
        .flashcard-item-actions {
            display: flex;
            gap: 6px;
        }
        .flashcard-item-btn {
            background: var(--bg);
            border: none;
            width: 32px;
            height: 32px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 0.9rem;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.2s;
        }
        .flashcard-item-btn:hover { background: var(--primary); color: white; }

        /* STUDY MODE - FIXED: Now outside app-container */
        .study-container {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            padding: 20px;
            z-index: 200;
            animation: fadeIn 0.4s ease;
            flex-direction: column;
        }
        .study-container.active {
            display: flex;
        }
        .study-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            color: white;
            margin-bottom: 20px;
        }
        .study-progress {
            background: rgba(255,255,255,0.2);
            height: 6px;
            border-radius: 3px;
            margin-bottom: 20px;
            overflow: hidden;
        }
        .study-progress-bar {
            height: 100%;
            background: white;
            border-radius: 3px;
            transition: width 0.3s ease;
        }
        .card-container {
            flex: 1;
            perspective: 1000px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 20px;
        }
        .card-flipper {
            width: 100%;
            max-width: 360px;
            height: 420px;
            position: relative;
            transform-style: preserve-3d;
            transition: transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);
            cursor: pointer;
        }
        .card-flipper.flipped { transform: rotateY(180deg); }
        .card-face {
            position: absolute;
            width: 100%;
            height: 100%;
            backface-visibility: hidden;
            background: white;
            border-radius: 24px;
            padding: 24px;
            box-shadow: 0 25px 50px -12px rgba(0,0,0,0.25);
            display: flex;
            flex-direction: column;
            overflow: hidden;
        }
        .card-face.back { transform: rotateY(180deg); }
        .card-label {
            font-size: 0.7rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            color: var(--text-secondary);
            margin-bottom: 12px;
            font-weight: 700;
        }
        .card-content {
            flex: 1;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            overflow-y: auto;
            word-break: break-word;
        }
        .card-text {
            font-size: 1.3rem;
            line-height: 1.6;
            color: var(--text);
            width: 100%;
        }
        .card-image {
            max-width: 100%;
            max-height: 200px;
            border-radius: 12px;
            margin: 10px 0;
            object-fit: contain;
        }
        .card-image.cover { object-fit: cover; width: 100%; height: 180px; }
        .card-image.contain { object-fit: contain; }
        .card-image.fill { object-fit: fill; width: 100%; height: 180px; }
        .card-link {
            color: var(--primary);
            text-decoration: none;
            font-size: 0.85rem;
            word-break: break-all;
            margin-top: 8px;
            display: inline-flex;
            align-items: center;
            gap: 4px;
        }
        .card-link::before { content: "🔗"; }
        .study-controls {
            display: flex;
            gap: 12px;
            justify-content: center;
        }
        .study-btn {
            flex: 1;
            max-width: 120px;
            padding: 14px 20px;
            border: none;
            border-radius: 14px;
            font-size: 0.9rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s;
            color: white;
        }
        .study-btn.prev { background: rgba(255,255,255,0.2); }
        .study-btn.flip { background: white; color: var(--primary); }
        .study-btn.next { background: rgba(255,255,255,0.2); }
        .study-btn:active { transform: scale(0.95); }
        .study-btn:disabled { opacity: 0.4; cursor: not-allowed; }

        .modal-overlay {
            display: none;
            position: fixed;
            inset: 0;
            background: rgba(0,0,0,0.6);
            backdrop-filter: blur(4px);
            z-index: 1000;
            align-items: flex-end;
            justify-content: center;
            animation: fadeIn 0.2s ease;
        }
        .modal-overlay.active { display: flex; }
        .modal {
            background: var(--surface);
            width: 100%;
            max-width: 480px;
            max-height: 90vh;
            border-radius: 24px 24px 0 0;
            padding: 24px;
            animation: slideUp 0.3s ease;
            overflow-y: auto;
            display: flex;
            flex-direction: column;
        }
        .modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
        }
        .modal-title { font-size: 1.2rem; font-weight: 700; }
        .modal-close {
            background: var(--bg);
            border: none;
            width: 36px;
            height: 36px;
            border-radius: 10px;
            cursor: pointer;
            font-size: 1.2rem;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .form-group { margin-bottom: 16px; }
        .form-label {
            display: block;
            font-size: 0.85rem;
            font-weight: 600;
            margin-bottom: 6px;
            color: var(--text-secondary);
        }
        .form-input, .form-textarea {
            width: 100%;
            padding: 12px 14px;
            border: 2px solid var(--border);
            border-radius: 12px;
            font-size: 0.95rem;
            font-family: inherit;
            transition: border-color 0.2s;
            background: var(--bg);
        }
        .form-input:focus, .form-textarea:focus {
            outline: none;
            border-color: var(--primary);
        }
        .form-textarea {
            min-height: 100px;
            resize: vertical;
        }

        .image-upload-area {
            border: 2px dashed var(--border);
            border-radius: 12px;
            padding: 20px;
            text-align: center;
            cursor: pointer;
            transition: all 0.2s;
            background: var(--bg);
        }
        .image-upload-area:hover { border-color: var(--primary); background: rgba(99,102,241,0.05); }
        .image-upload-area.has-image {
            border-style: solid;
            border-color: var(--primary);
            padding: 10px;
        }
        .upload-preview {
            max-width: 100%;
            max-height: 150px;
            border-radius: 8px;
            margin-bottom: 8px;
        }
        .upload-hint { color: var(--text-secondary); font-size: 0.85rem; }
        .upload-input { display: none; }

        .fit-options {
            display: flex;
            gap: 8px;
            margin-top: 8px;
        }
        .fit-option {
            flex: 1;
            padding: 8px;
            border: 2px solid var(--border);
            border-radius: 8px;
            text-align: center;
            cursor: pointer;
            font-size: 0.8rem;
            transition: all 0.2s;
            background: var(--bg);
        }
        .fit-option.active {
            border-color: var(--primary);
            background: rgba(99,102,241,0.1);
            color: var(--primary);
            font-weight: 600;
        }

        .color-picker {
            display: flex;
            gap: 8px;
            flex-wrap: wrap;
        }
        .color-option {
            width: 36px;
            height: 36px;
            border-radius: 10px;
            cursor: pointer;
            border: 3px solid transparent;
            transition: all 0.2s;
        }
        .color-option.active { border-color: var(--text); transform: scale(1.1); }

        .btn {
            width: 100%;
            padding: 14px;
            border: none;
            border-radius: 12px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }
        .btn-primary {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            box-shadow: 0 4px 15px rgba(99,102,241,0.4);
        }
        .btn-primary:hover { transform: translateY(-1px); box-shadow: 0 6px 20px rgba(99,102,241,0.5); }
        .btn-primary:active { transform: translateY(0); }
        .btn-secondary {
            background: var(--bg);
            color: var(--text);
            border: 2px solid var(--border);
        }
        .btn-danger { background: #ef4444; color: white; }
        .btn-success { background: #10b981; color: white; }

        .fab {
            position: fixed;
            bottom: 24px;
            right: 24px;
            width: 56px;
            height: 56px;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
            box-shadow: 0 4px 15px rgba(99,102,241,0.4);
            transition: all 0.2s;
            z-index: 50;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .fab:hover { transform: scale(1.1) rotate(90deg); }
        .fab:active { transform: scale(0.95); }

        .tabs {
            display: flex;
            gap: 4px;
            background: var(--bg);
            padding: 4px;
            border-radius: 12px;
            margin-bottom: 16px;
        }
        .tab {
            flex: 1;
            padding: 10px;
            border: none;
            background: none;
            border-radius: 8px;
            font-size: 0.85rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s;
            color: var(--text-secondary);
        }
        .tab.active { background: white; color: var(--primary); box-shadow: var(--shadow); }

        .editor-preview {
            background: var(--bg);
            border-radius: 12px;
            padding: 16px;
            margin-bottom: 16px;
            border: 2px solid var(--border);
        }
        .preview-label {
            font-size: 0.7rem;
            text-transform: uppercase;
            color: var(--text-secondary);
            margin-bottom: 8px;
            font-weight: 700;
        }
        .preview-content {
            min-height: 80px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            word-break: break-word;
        }

        .toast {
            position: fixed;
            bottom: 90px;
            left: 50%;
            transform: translateX(-50%) translateY(100px);
            background: var(--text);
            color: white;
            padding: 12px 24px;
            border-radius: 12px;
            font-size: 0.9rem;
            z-index: 2000;
            opacity: 0;
            transition: all 0.3s ease;
            white-space: nowrap;
        }
        .toast.show { transform: translateX(-50%) translateY(0); opacity: 1; }

        @media (max-width: 480px) {
            .app-container { max-width: 100%; }
            .folders-grid { grid-template-columns: repeat(2, 1fr); gap: 10px; }
            .card-flipper { height: 380px; }
        }

        .card-content::-webkit-scrollbar { width: 4px; }
        .card-content::-webkit-scrollbar-thumb { background: var(--border); border-radius: 2px; }

        .hidden { display: none !important; }

        .breadcrumb {
            display: flex;
            align-items: center;
            gap: 8px;
            padding: 8px 16px;
            background: var(--surface);
            border-bottom: 1px solid var(--border);
            font-size: 0.85rem;
        }
        .breadcrumb-item {
            color: var(--text-secondary);
            cursor: pointer;
            transition: color 0.2s;
        }
        .breadcrumb-item:hover { color: var(--primary); }
        .breadcrumb-item.active { color: var(--text); font-weight: 600; }
        .breadcrumb-separator { color: var(--text-secondary); }

        .stats-bar {
            display: flex;
            justify-content: space-around;
            padding: 12px;
            background: var(--surface);
            border-bottom: 1px solid var(--border);
        }
        .stat-item { text-align: center; }
        .stat-value { font-size: 1.2rem; font-weight: 700; color: var(--primary); }
        .stat-label { font-size: 0.7rem; color: var(--text-secondary); text-transform: uppercase; }

        .link-input-group {
            display: flex;
            gap: 8px;
        }
        .link-input-group .form-input { flex: 1; }
        .link-input-group .btn {
            width: auto;
            padding: 12px 16px;
            white-space: nowrap;
        }

        .study-action-bar {
            display: flex;
            gap: 10px;
            margin-bottom: 15px;
        }
        .study-action-btn {
            flex: 1;
            padding: 10px;
            border: none;
            border-radius: 10px;
            background: rgba(255,255,255,0.15);
            color: white;
            font-size: 0.8rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s;
        }
        .study-action-btn:hover { background: rgba(255,255,255,0.25); }
    </style>
<base target="_blank">
</head>
<body>
    <!-- Main App Container -->
    <div class="app-container" id="appContainer">
        <header class="header">
            <h1><span class="header-icon">🧠</span> FlashMind</h1>
            <div class="header-actions">
                <button class="btn-icon" onclick="app.toggleSearch()" title="Buscar">🔍</button>
                <button class="btn-icon" onclick="app.showImportExport()" title="Importar/Exportar">💾</button>
            </div>
        </header>

        <div class="search-container hidden" id="searchContainer">
            <div class="search-box">
                <span>🔍</span>
                <input type="text" id="searchInput" placeholder="Buscar en flashcards..." oninput="app.handleSearch(this.value)">
                <button class="search-clear" id="searchClear" onclick="app.clearSearch()">✕</button>
            </div>
        </div>

        <div class="breadcrumb hidden" id="breadcrumb">
            <span class="breadcrumb-item" onclick="app.goHome()">📁 Carpetas</span>
            <span class="breadcrumb-separator">›</span>
            <span class="breadcrumb-item active" id="breadcrumbFolder"></span>
        </div>

        <div class="stats-bar hidden" id="statsBar">
            <div class="stat-item">
                <div class="stat-value" id="statTotal">0</div>
                <div class="stat-label">Total</div>
            </div>
            <div class="stat-item">
                <div class="stat-value" id="statFolders">0</div>
                <div class="stat-label">Carpetas</div>
            </div>
        </div>

        <main class="content" id="mainContent">
            <div id="foldersView">
                <div class="empty-state" id="foldersEmpty">
                    <div class="icon">📂</div>
                    <h3>No hay carpetas</h3>
                    <p>Crea tu primera carpeta para organizar tus flashcards</p>
                </div>
                <div class="folders-grid" id="foldersGrid"></div>
            </div>

            <div id="flashcardsView" class="hidden">
                <div class="empty-state" id="flashcardsEmpty">
                    <div class="icon">📝</div>
                    <h3>No hay flashcards</h3>
                    <p>Agrega flashcards a esta carpeta para comenzar a estudiar</p>
                </div>
                <div class="flashcards-list" id="flashcardsList"></div>
            </div>
        </main>

        <button class="fab" id="fab" onclick="app.handleFabClick()">+</button>
    </div>

    <!-- Study Mode - FIXED: Now outside app-container with fixed positioning -->
    <div class="study-container" id="studyContainer">
        <div class="study-header">
            <button class="btn-icon" onclick="app.exitStudy()" style="background:rgba(255,255,255,0.2);">✕</button>
            <span id="studyCounter">1 / 1</span>
            <button class="btn-icon" onclick="app.shuffleCards()" style="background:rgba(255,255,255,0.2);" title="Aleatorio">🔀</button>
        </div>
        <div class="study-progress">
            <div class="study-progress-bar" id="studyProgressBar" style="width: 0%"></div>
        </div>
        <div class="study-action-bar">
            <button class="study-action-btn" onclick="app.studyFolder()">📚 Estudiar Carpeta</button>
        </div>
        <div class="card-container" onclick="app.flipCard()">
            <div class="card-flipper" id="cardFlipper">
                <div class="card-face front">
                    <div class="card-label">Frente</div>
                    <div class="card-content" id="cardFrontContent"></div>
                </div>
                <div class="card-face back">
                    <div class="card-label">Reverso</div>
                    <div class="card-content" id="cardBackContent"></div>
                </div>
            </div>
        </div>
        <div class="study-controls">
            <button class="study-btn prev" onclick="app.prevCard()" id="btnPrev">◀ Anterior</button>
            <button class="study-btn flip" onclick="app.flipCard()">↻ Voltear</button>
            <button class="study-btn next" onclick="app.nextCard()" id="btnNext">Siguiente ▶</button>
        </div>
    </div>

    <div class="toast" id="toast"></div>

    <!-- Modals -->
    <div class="modal-overlay" id="folderModal">
        <div class="modal">
            <div class="modal-header">
                <h3 class="modal-title" id="folderModalTitle">Nueva Carpeta</h3>
                <button class="modal-close" onclick="app.closeModal('folderModal')">✕</button>
            </div>
            <div class="form-group">
                <label class="form-label">Nombre</label>
                <input type="text" class="form-input" id="folderName" placeholder="Ej: Inglés, Biología, Historia...">
            </div>
            <div class="form-group">
                <label class="form-label">Color</label>
                <div class="color-picker" id="folderColors"></div>
            </div>
            <div class="form-group">
                <label class="form-label">Icono</label>
                <div class="color-picker" id="folderIcons" style="font-size: 1.3rem;"></div>
            </div>
            <button class="btn btn-primary" onclick="app.saveFolder()">💾 Guardar Carpeta</button>
        </div>
    </div>

    <div class="modal-overlay" id="flashcardModal">
        <div class="modal" style="max-height: 95vh;">
            <div class="modal-header">
                <h3 class="modal-title" id="flashcardModalTitle">Nueva Flashcard</h3>
                <button class="modal-close" onclick="app.closeModal('flashcardModal')">✕</button>
            </div>

            <div class="tabs">
                <button class="tab active" onclick="app.switchTab('front')" id="tabFront">Frente</button>
                <button class="tab" onclick="app.switchTab('back')" id="tabBack">Reverso</button>
            </div>

            <div id="frontEditor">
                <div class="editor-preview">
                    <div class="preview-label">Vista previa - Frente</div>
                    <div class="preview-content" id="previewFront"></div>
                </div>
                <div class="form-group">
                    <label class="form-label">Texto (soporta emojis ✨🎉)</label>
                    <textarea class="form-textarea" id="frontText" placeholder="Escribe el contenido del frente..." oninput="app.updatePreview()"></textarea>
                </div>
                <div class="form-group">
                    <label class="form-label">Imagen</label>
                    <div class="image-upload-area" id="frontImageArea" onclick="app.triggerUpload('front')">
                        <div id="frontImagePreview"></div>
                        <div class="upload-hint" id="frontImageHint">📷 Toca para subir imagen</div>
                    </div>
                    <input type="file" class="upload-input" id="frontImageInput" accept="image/*" onchange="app.handleImageUpload(this, 'front')">
                    <div class="fit-options" id="frontFitOptions">
                        <div class="fit-option active" onclick="app.setImageFit('front', 'contain')">Ajustar</div>
                        <div class="fit-option" onclick="app.setImageFit('front', 'cover')">Cubrir</div>
                        <div class="fit-option" onclick="app.setImageFit('front', 'fill')">Llenar</div>
                    </div>
                </div>
                <div class="form-group">
                    <label class="form-label">Enlace</label>
                    <div class="link-input-group">
                        <input type="text" class="form-input" id="frontLink" placeholder="https://..." oninput="app.updatePreview()">
                    </div>
                </div>
            </div>

            <div id="backEditor" class="hidden">
                <div class="editor-preview">
                    <div class="preview-label">Vista previa - Reverso</div>
                    <div class="preview-content" id="previewBack"></div>
                </div>
                <div class="form-group">
                    <label class="form-label">Texto (soporta emojis ✨🎉)</label>
                    <textarea class="form-textarea" id="backText" placeholder="Escribe el contenido del reverso..." oninput="app.updatePreview()"></textarea>
                </div>
                <div class="form-group">
                    <label class="form-label">Imagen</label>
                    <div class="image-upload-area" id="backImageArea" onclick="app.triggerUpload('back')">
                        <div id="backImagePreview"></div>
                        <div class="upload-hint" id="backImageHint">📷 Toca para subir imagen</div>
                    </div>
                    <input type="file" class="upload-input" id="backImageInput" accept="image/*" onchange="app.handleImageUpload(this, 'back')">
                    <div class="fit-options" id="backFitOptions">
                        <div class="fit-option active" onclick="app.setImageFit('back', 'contain')">Ajustar</div>
                        <div class="fit-option" onclick="app.setImageFit('back', 'cover')">Cubrir</div>
                        <div class="fit-option" onclick="app.setImageFit('back', 'fill')">Llenar</div>
                    </div>
                </div>
                <div class="form-group">
                    <label class="form-label">Enlace</label>
                    <div class="link-input-group">
                        <input type="text" class="form-input" id="backLink" placeholder="https://..." oninput="app.updatePreview()">
                    </div>
                </div>
            </div>

            <button class="btn btn-primary" onclick="app.saveFlashcard()" style="margin-top: 8px;">💾 Guardar Flashcard</button>
        </div>
    </div>

    <div class="modal-overlay" id="dataModal">
        <div class="modal">
            <div class="modal-header">
                <h3 class="modal-title">Importar / Exportar Datos</h3>
                <button class="modal-close" onclick="app.closeModal('dataModal')">✕</button>
            </div>
            <div class="form-group">
                <label class="form-label">Exportar datos</label>
                <button class="btn btn-secondary" onclick="app.exportData()">📥 Descargar JSON</button>
            </div>
            <div class="form-group">
                <label class="form-label">Importar datos</label>
                <div class="image-upload-area" onclick="document.getElementById('importFile').click()">
                    <div class="upload-hint">📤 Seleccionar archivo JSON</div>
                </div>
                <input type="file" class="upload-input" id="importFile" accept=".json" onchange="app.importData(this)">
            </div>
            <button class="btn btn-danger" onclick="app.clearAllData()">🗑️ Borrar todos los datos</button>
        </div>
    </div>

    <script>
        class FlashMindApp {
            constructor() {
                this.data = this.loadData();
                this.currentFolder = null;
                this.currentFlashcard = null;
                this.studyIndex = 0;
                this.studyCards = [];
                this.isFlipped = false;
                this.searchQuery = '';
                this.currentTab = 'front';
                this.tempImages = { front: null, back: null };
                this.imageFits = { front: 'contain', back: 'contain' };
                this.colors = ['#6366f1', '#8b5cf6', '#ec4899', '#f43f5e', '#f97316', '#eab308', '#22c55e', '#06b6d4', '#3b82f6', '#a855f7'];
                this.icons = ['📚', '📖', '🧮', '🌍', '🔬', '🎨', '🎵', '💻', '🏃', '🍎', '⭐', '🔥', '💡', '🎯', '🚀'];
                this.selectedColor = this.colors[0];
                this.selectedIcon = this.icons[0];
                this.editingFolderId = null;
                this.editingFlashcardId = null;
                this.init();
            }

            init() {
                this.renderFolders();
                this.renderColorPicker();
                this.renderIconPicker();
                this.updateStats();

                document.addEventListener('keydown', (e) => {
                    if (document.getElementById('studyContainer').style.display === 'flex') {
                        if (e.key === ' ' || e.key === 'Enter') {
                            e.preventDefault();
                            this.flipCard();
                        } else if (e.key === 'ArrowLeft') {
                            this.prevCard();
                        } else if (e.key === 'ArrowRight') {
                            this.nextCard();
                        }
                    }
                });

                let touchStartX = 0;
                let touchEndX = 0;
                const studyContainer = document.getElementById('studyContainer');
                studyContainer.addEventListener('touchstart', (e) => {
                    touchStartX = e.changedTouches[0].screenX;
                }, {passive: true});
                studyContainer.addEventListener('touchend', (e) => {
                    touchEndX = e.changedTouches[0].screenX;
                    this.handleSwipe(touchStartX, touchEndX);
                }, {passive: true});
            }

            handleSwipe(start, end) {
                const diff = start - end;
                if (Math.abs(diff) > 50) {
                    if (diff > 0) this.nextCard();
                    else this.prevCard();
                }
            }

            loadData() {
                try {
                    const saved = localStorage.getItem('flashmind_data');
                    if (saved) return JSON.parse(saved);
                } catch(e) {}
                return { folders: [], flashcards: [] };
            }

            saveData() {
                localStorage.setItem('flashmind_data', JSON.stringify(this.data));
                this.updateStats();
            }

            updateStats() {
                document.getElementById('statTotal').textContent = this.data.flashcards.length;
                document.getElementById('statFolders').textContent = this.data.folders.length;
            }

            renderFolders() {
                const grid = document.getElementById('foldersGrid');
                const empty = document.getElementById('foldersEmpty');

                if (this.data.folders.length === 0) {
                    grid.innerHTML = '';
                    empty.style.display = 'block';
                    return;
                }

                empty.style.display = 'none';
                grid.innerHTML = this.data.folders.map(folder => {
                    const count = this.data.flashcards.filter(f => f.folderId === folder.id).length;
                    return `
                        <div class="folder-card" onclick="app.openFolder('${folder.id}')">
                            <div class="folder-actions" onclick="event.stopPropagation()">
                                <button class="folder-action-btn" onclick="app.editFolder('${folder.id}')">✏️</button>
                                <button class="folder-action-btn" onclick="app.deleteFolder('${folder.id}')">🗑️</button>
                            </div>
                            <div class="folder-icon" style="background: ${folder.color}20; color: ${folder.color};">
                                ${folder.icon}
                            </div>
                            <div class="folder-name">${this.escapeHtml(folder.name)}</div>
                            <div class="folder-count">${count} flashcard${count !== 1 ? 's' : ''}</div>
                        </div>
                    `;
                }).join('');
            }

            renderColorPicker() {
                const container = document.getElementById('folderColors');
                container.innerHTML = this.colors.map((color, i) => `
                    <div class="color-option ${i === 0 ? 'active' : ''}" 
                         style="background: ${color}" 
                         onclick="app.selectColor('${color}', this)"></div>
                `).join('');
            }

            renderIconPicker() {
                const container = document.getElementById('folderIcons');
                container.innerHTML = this.icons.map((icon, i) => `
                    <div class="color-option ${i === 0 ? 'active' : ''}" 
                         style="display:flex;align-items:center;justify-content:center;font-size:1.2rem;"
                         onclick="app.selectIcon('${icon}', this)">${icon}</div>
                `).join('');
            }

            selectColor(color, el) {
                this.selectedColor = color;
                document.querySelectorAll('#folderColors .color-option').forEach(c => c.classList.remove('active'));
                el.classList.add('active');
            }

            selectIcon(icon, el) {
                this.selectedIcon = icon;
                document.querySelectorAll('#folderIcons .color-option').forEach(c => c.classList.remove('active'));
                el.classList.add('active');
            }

            showFolderModal() {
                this.editingFolderId = null;
                document.getElementById('folderModalTitle').textContent = 'Nueva Carpeta';
                document.getElementById('folderName').value = '';
                this.selectedColor = this.colors[0];
                this.selectedIcon = this.icons[0];
                this.renderColorPicker();
                this.renderIconPicker();
                this.openModal('folderModal');
            }

            editFolder(id) {
                const folder = this.data.folders.find(f => f.id === id);
                if (!folder) return;
                this.editingFolderId = id;
                document.getElementById('folderModalTitle').textContent = 'Editar Carpeta';
                document.getElementById('folderName').value = folder.name;
                this.selectedColor = folder.color;
                this.selectedIcon = folder.icon;
                this.openModal('folderModal');
            }

            saveFolder() {
                const name = document.getElementById('folderName').value.trim();
                if (!name) {
                    this.showToast('❌ Ingresa un nombre');
                    return;
                }

                if (this.editingFolderId) {
                    const folder = this.data.folders.find(f => f.id === this.editingFolderId);
                    folder.name = name;
                    folder.color = this.selectedColor;
                    folder.icon = this.selectedIcon;
                } else {
                    this.data.folders.push({
                        id: Date.now().toString(),
                        name,
                        color: this.selectedColor,
                        icon: this.selectedIcon,
                        createdAt: new Date().toISOString()
                    });
                }

                this.saveData();
                this.renderFolders();
                this.closeModal('folderModal');
                this.showToast(this.editingFolderId ? '✅ Carpeta actualizada' : '✅ Carpeta creada');
            }

            deleteFolder(id) {
                if (!confirm('¿Eliminar esta carpeta y todas sus flashcards?')) return;
                this.data.folders = this.data.folders.filter(f => f.id !== id);
                this.data.flashcards = this.data.flashcards.filter(f => f.folderId !== id);
                this.saveData();
                this.renderFolders();
                this.showToast('🗑️ Carpeta eliminada');
            }

            openFolder(id) {
                this.currentFolder = id;
                const folder = this.data.folders.find(f => f.id === id);
                document.getElementById('breadcrumbFolder').textContent = folder.icon + ' ' + folder.name;
                document.getElementById('breadcrumb').classList.remove('hidden');
                document.getElementById('foldersView').classList.add('hidden');
                document.getElementById('flashcardsView').classList.remove('hidden');
                document.getElementById('statsBar').classList.remove('hidden');
                this.renderFlashcards();
            }

            goHome() {
                this.currentFolder = null;
                document.getElementById('breadcrumb').classList.add('hidden');
                document.getElementById('foldersView').classList.remove('hidden');
                document.getElementById('flashcardsView').classList.add('hidden');
                document.getElementById('statsBar').classList.add('hidden');
                this.renderFolders();
            }

            renderFlashcards() {
                const list = document.getElementById('flashcardsList');
                const empty = document.getElementById('flashcardsEmpty');
                let cards = this.data.flashcards.filter(f => f.folderId === this.currentFolder);

                if (this.searchQuery) {
                    const q = this.searchQuery.toLowerCase();
                    cards = cards.filter(f => 
                        (f.front.text && f.front.text.toLowerCase().includes(q)) ||
                        (f.back.text && f.back.text.toLowerCase().includes(q))
                    );
                }

                if (cards.length === 0) {
                    list.innerHTML = '';
                    empty.style.display = 'block';
                    empty.querySelector('h3').textContent = this.searchQuery ? 'No se encontraron resultados' : 'No hay flashcards';
                    return;
                }

                empty.style.display = 'none';
                list.innerHTML = cards.map(card => {
                    const hasImage = card.front.image || card.back.image;
                    const preview = card.front.text || card.back.text || 'Sin texto';
                    const backPreview = card.back.text || '';
                    return `
                        <div class="flashcard-item">
                            <div class="flashcard-preview" style="background: linear-gradient(135deg, ${this.getFolderColor()}, var(--secondary));">
                                ${hasImage ? '🖼️' : '📝'}
                            </div>
                            <div class="flashcard-info" onclick="app.studyCard('${card.id}')">
                                <div class="flashcard-front">${this.escapeHtml(preview.substring(0, 50))}${preview.length > 50 ? '...' : ''}</div>
                                <div class="flashcard-back-preview">${this.escapeHtml(backPreview.substring(0, 40))}${backPreview.length > 40 ? '...' : ''}</div>
                            </div>
                            <div class="flashcard-item-actions">
                                <button class="flashcard-item-btn" onclick="app.editFlashcard('${card.id}')">✏️</button>
                                <button class="flashcard-item-btn" onclick="app.deleteFlashcard('${card.id}')">🗑️</button>
                            </div>
                        </div>
                    `;
                }).join('');
            }

            getFolderColor() {
                const folder = this.data.folders.find(f => f.id === this.currentFolder);
                return folder ? folder.color : 'var(--primary)';
            }

            showFlashcardModal() {
                this.editingFlashcardId = null;
                this.currentTab = 'front';
                this.tempImages = { front: null, back: null };
                this.imageFits = { front: 'contain', back: 'contain' };
                document.getElementById('flashcardModalTitle').textContent = 'Nueva Flashcard';
                document.getElementById('frontText').value = '';
                document.getElementById('backText').value = '';
                document.getElementById('frontLink').value = '';
                document.getElementById('backLink').value = '';
                this.clearImagePreview('front');
                this.clearImagePreview('back');
                this.switchTab('front');
                this.updatePreview();
                this.openModal('flashcardModal');
            }

            editFlashcard(id) {
                const card = this.data.flashcards.find(f => f.id === id);
                if (!card) return;
                this.editingFlashcardId = id;
                this.currentTab = 'front';
                this.tempImages = { front: card.front.image || null, back: card.back.image || null };
                this.imageFits = { 
                    front: card.front.imageFit || 'contain', 
                    back: card.back.imageFit || 'contain' 
                };
                document.getElementById('flashcardModalTitle').textContent = 'Editar Flashcard';
                document.getElementById('frontText').value = card.front.text || '';
                document.getElementById('backText').value = card.back.text || '';
                document.getElementById('frontLink').value = card.front.link || '';
                document.getElementById('backLink').value = card.back.link || '';

                if (card.front.image) this.showImagePreview('front', card.front.image);
                else this.clearImagePreview('front');
                if (card.back.image) this.showImagePreview('back', card.back.image);
                else this.clearImagePreview('back');

                this.updateFitOptions('front', this.imageFits.front);
                this.updateFitOptions('back', this.imageFits.back);
                this.switchTab('front');
                this.updatePreview();
                this.openModal('flashcardModal');
            }

            saveFlashcard() {
                const frontText = document.getElementById('frontText').value.trim();
                const backText = document.getElementById('backText').value.trim();
                const frontLink = document.getElementById('frontLink').value.trim();
                const backLink = document.getElementById('backLink').value.trim();

                if (!frontText && !this.tempImages.front && !frontLink && !backText && !this.tempImages.back && !backLink) {
                    this.showToast('❌ La flashcard está vacía');
                    return;
                }

                const cardData = {
                    id: this.editingFlashcardId || Date.now().toString(),
                    folderId: this.currentFolder,
                    front: {
                        text: frontText,
                        image: this.tempImages.front,
                        imageFit: this.imageFits.front,
                        link: frontLink || null
                    },
                    back: {
                        text: backText,
                        image: this.tempImages.back,
                        imageFit: this.imageFits.back,
                        link: backLink || null
                    },
                    createdAt: new Date().toISOString()
                };

                if (this.editingFlashcardId) {
                    const idx = this.data.flashcards.findIndex(f => f.id === this.editingFlashcardId);
                    this.data.flashcards[idx] = cardData;
                } else {
                    this.data.flashcards.push(cardData);
                }

                this.saveData();
                this.renderFlashcards();
                this.closeModal('flashcardModal');
                this.showToast(this.editingFlashcardId ? '✅ Flashcard actualizada' : '✅ Flashcard creada');
            }

            deleteFlashcard(id) {
                if (!confirm('¿Eliminar esta flashcard?')) return;
                this.data.flashcards = this.data.flashcards.filter(f => f.id !== id);
                this.saveData();
                this.renderFlashcards();
                this.showToast('🗑️ Flashcard eliminada');
            }

            triggerUpload(side) {
                document.getElementById(side + 'ImageInput').click();
            }

            handleImageUpload(input, side) {
                const file = input.files[0];
                if (!file) return;

                const reader = new FileReader();
                reader.onload = (e) => {
                    this.tempImages[side] = e.target.result;
                    this.showImagePreview(side, e.target.result);
                    this.updatePreview();
                };
                reader.readAsDataURL(file);
                input.value = '';
            }

            showImagePreview(side, src) {
                const area = document.getElementById(side + 'ImageArea');
                const preview = document.getElementById(side + 'ImagePreview');
                const hint = document.getElementById(side + 'ImageHint');
                area.classList.add('has-image');
                preview.innerHTML = `<img src="${src}" class="upload-preview">`;
                hint.textContent = '📷 Toca para cambiar imagen';
            }

            clearImagePreview(side) {
                const area = document.getElementById(side + 'ImageArea');
                const preview = document.getElementById(side + 'ImagePreview');
                const hint = document.getElementById(side + 'ImageHint');
                area.classList.remove('has-image');
                preview.innerHTML = '';
                hint.textContent = '📷 Toca para subir imagen';
            }

            setImageFit(side, fit) {
                this.imageFits[side] = fit;
                this.updateFitOptions(side, fit);
                this.updatePreview();
            }

            updateFitOptions(side, activeFit) {
                const container = document.getElementById(side + 'FitOptions');
                container.querySelectorAll('.fit-option').forEach(opt => {
                    opt.classList.toggle('active', opt.textContent === this.getFitLabel(activeFit));
                });
            }

            getFitLabel(fit) {
                const labels = { contain: 'Ajustar', cover: 'Cubrir', fill: 'Llenar' };
                return labels[fit] || 'Ajustar';
            }

            switchTab(tab) {
                this.currentTab = tab;
                document.getElementById('tabFront').classList.toggle('active', tab === 'front');
                document.getElementById('tabBack').classList.toggle('active', tab === 'back');
                document.getElementById('frontEditor').classList.toggle('hidden', tab !== 'front');
                document.getElementById('backEditor').classList.toggle('hidden', tab !== 'back');
            }

            updatePreview() {
                const frontText = document.getElementById('frontText').value;
                const backText = document.getElementById('backText').value;
                const frontLink = document.getElementById('frontLink').value;
                const backLink = document.getElementById('backLink').value;

                document.getElementById('previewFront').innerHTML = this.buildPreviewHtml({
                    text: frontText,
                    image: this.tempImages.front,
                    imageFit: this.imageFits.front,
                    link: frontLink
                });
                document.getElementById('previewBack').innerHTML = this.buildPreviewHtml({
                    text: backText,
                    image: this.tempImages.back,
                    imageFit: this.imageFits.back,
                    link: backLink
                });
            }

            buildPreviewHtml(data) {
                let html = '';
                if (data.text) {
                    html += `<div style="font-size:1rem;line-height:1.5;margin-bottom:8px;">${this.escapeHtml(data.text).replace(/\n/g, '<br>')}</div>`;
                }
                if (data.image) {
                    html += `<img src="${data.image}" class="card-image ${data.imageFit || 'contain'}" style="max-height:100px;">`;
                }
                if (data.link) {
                    html += `<a href="${data.link}" target="_blank" class="card-link" style="font-size:0.75rem;">${data.link}</a>`;
                }
                return html || '<span style="color:var(--text-secondary);">Vista previa vacía</span>';
            }

            studyCard(cardId) {
                const card = this.data.flashcards.find(f => f.id === cardId);
                if (!card) return;
                this.studyCards = [card];
                this.studyIndex = 0;
                this.startStudy();
            }

            studyFolder() {
                const cards = this.data.flashcards.filter(f => f.folderId === this.currentFolder);
                if (cards.length === 0) {
                    this.showToast('❌ No hay flashcards para estudiar');
                    return;
                }
                this.studyCards = [...cards];
                this.studyIndex = 0;
                this.startStudy();
            }

            startStudy() {
                // FIXED: Use classList to show study container
                document.getElementById('studyContainer').classList.add('active');
                document.getElementById('appContainer').style.display = 'none';
                this.isFlipped = false;
                this.updateStudyCard();
            }

            exitStudy() {
                // FIXED: Use classList to hide study container
                document.getElementById('studyContainer').classList.remove('active');
                document.getElementById('appContainer').style.display = 'flex';
                this.isFlipped = false;
                document.getElementById('cardFlipper').classList.remove('flipped');
            }

            updateStudyCard() {
                const card = this.studyCards[this.studyIndex];
                const flipper = document.getElementById('cardFlipper');

                this.isFlipped = false;
                flipper.classList.remove('flipped');

                document.getElementById('cardFrontContent').innerHTML = this.buildCardContent(card.front);
                document.getElementById('cardBackContent').innerHTML = this.buildCardContent(card.back);

                document.getElementById('studyCounter').textContent = `${this.studyIndex + 1} / ${this.studyCards.length}`;
                document.getElementById('studyProgressBar').style.width = `${((this.studyIndex + 1) / this.studyCards.length) * 100}%`;

                document.getElementById('btnPrev').disabled = this.studyIndex === 0;
                document.getElementById('btnNext').disabled = this.studyIndex === this.studyCards.length - 1;
            }

            buildCardContent(data) {
                let html = '';
                if (data.text) {
                    html += `<div class="card-text">${this.escapeHtml(data.text).replace(/\n/g, '<br>')}</div>`;
                }
                if (data.image) {
                    html += `<img src="${data.image}" class="card-image ${data.imageFit || 'contain'}">`;
                }
                if (data.link) {
                    html += `<a href="${data.link}" target="_blank" class="card-link">${data.link}</a>`;
                }
                return html || '<span style="color:var(--text-secondary);">Sin contenido</span>';
            }

            flipCard() {
                this.isFlipped = !this.isFlipped;
                document.getElementById('cardFlipper').classList.toggle('flipped', this.isFlipped);
            }

            nextCard() {
                if (this.studyIndex < this.studyCards.length - 1) {
                    this.studyIndex++;
                    this.updateStudyCard();
                }
            }

            prevCard() {
                if (this.studyIndex > 0) {
                    this.studyIndex--;
                    this.updateStudyCard();
                }
            }

            shuffleCards() {
                for (let i = this.studyCards.length - 1; i > 0; i--) {
                    const j = Math.floor(Math.random() * (i + 1));
                    [this.studyCards[i], this.studyCards[j]] = [this.studyCards[j], this.studyCards[i]];
                }
                this.studyIndex = 0;
                this.updateStudyCard();
                this.showToast('🔀 Cartas mezcladas');
            }

            toggleSearch() {
                const container = document.getElementById('searchContainer');
                container.classList.toggle('hidden');
                if (!container.classList.contains('hidden')) {
                    document.getElementById('searchInput').focus();
                } else {
                    this.clearSearch();
                }
            }

            handleSearch(query) {
                this.searchQuery = query;
                document.getElementById('searchClear').classList.toggle('visible', query.length > 0);
                if (this.currentFolder) {
                    this.renderFlashcards();
                }
            }

            clearSearch() {
                this.searchQuery = '';
                document.getElementById('searchInput').value = '';
                document.getElementById('searchClear').classList.remove('visible');
                if (this.currentFolder) {
                    this.renderFlashcards();
                }
            }

            handleFabClick() {
                if (this.currentFolder) {
                    this.showFlashcardModal();
                } else {
                    this.showFolderModal();
                }
            }

            showImportExport() {
                this.openModal('dataModal');
            }

            exportData() {
                const dataStr = JSON.stringify(this.data, null, 2);
                const blob = new Blob([dataStr], { type: 'application/json' });
                const url = URL.createObjectURL(blob);
                const a = document.createElement('a');
                a.href = url;
                a.download = `flashmind_backup_${new Date().toISOString().split('T')[0]}.json`;
                a.click();
                URL.revokeObjectURL(url);
                this.showToast('✅ Datos exportados');
            }

            importData(input) {
                const file = input.files[0];
                if (!file) return;

                const reader = new FileReader();
                reader.onload = (e) => {
                    try {
                        const data = JSON.parse(e.target.result);
                        if (data.folders && data.flashcards) {
                            this.data = data;
                            this.saveData();
                            this.renderFolders();
                            this.closeModal('dataModal');
                            this.showToast('✅ Datos importados correctamente');
                        } else {
                            throw new Error('Formato inválido');
                        }
                    } catch (err) {
                        this.showToast('❌ Error al importar: ' + err.message);
                    }
                };
                reader.readAsText(file);
                input.value = '';
            }

            clearAllData() {
                if (!confirm('¿Borrar TODOS los datos? Esta acción no se puede deshacer.')) return;
                this.data = { folders: [], flashcards: [] };
                this.saveData();
                this.goHome();
                this.closeModal('dataModal');
                this.showToast('🗑️ Todos los datos borrados');
            }

            openModal(id) {
                document.getElementById(id).classList.add('active');
                document.body.style.overflow = 'hidden';
            }

            closeModal(id) {
                document.getElementById(id).classList.remove('active');
                document.body.style.overflow = '';
            }

            showToast(message) {
                const toast = document.getElementById('toast');
                toast.textContent = message;
                toast.classList.add('show');
                setTimeout(() => toast.classList.remove('show'), 2500);
            }

            escapeHtml(text) {
                const div = document.createElement('div');
                div.textContent = text;
                return div.innerHTML;
            }
        }

        const app = new FlashMindApp();

        document.querySelectorAll('.modal-overlay').forEach(overlay => {
            overlay.addEventListener('click', (e) => {
                if (e.target === overlay) {
                    overlay.classList.remove('active');
                    document.body.style.overflow = '';
                }
            });
        });
    </script>
</body>
</html>
