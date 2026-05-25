<!DOCTYPE html>
<html lang="en" data-bs-theme="dark">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Domain Grouper</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;600&family=DM+Sans:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css" rel="stylesheet">
    <style>
        :root {
            --bg-deep: #0a0f0d;
            --bg-card: #111a16;
            --border-color: #1e2e27;
            --accent: #34d399;
            --accent-dim: rgba(52, 211, 153, 0.12);
            --accent-glow: rgba(52, 211, 153, 0.25);
            --text-primary: #e8f0ec;
            --text-secondary: #7a9489;
            --danger: #f87171;
            --danger-dim: rgba(248, 113, 113, 0.12);
            --warning: #fbbf24;
            --warning-dim: rgba(251, 191, 36, 0.12);
        }
        * { box-sizing: border-box; }
        body {
            font-family: 'DM Sans', sans-serif;
            background: var(--bg-deep);
            color: var(--text-primary);
            min-height: 100vh;
            overflow-x: hidden;
        }
        body::before {
            content: '';
            position: fixed; top: -40%; left: -20%;
            width: 80vw; height: 80vw;
            background: radial-gradient(circle, rgba(52,211,153,0.04) 0%, transparent 70%);
            pointer-events: none; z-index: 0;
        }
        body::after {
            content: '';
            position: fixed; bottom: -30%; right: -15%;
            width: 60vw; height: 60vw;
            background: radial-gradient(circle, rgba(52,211,153,0.03) 0%, transparent 70%);
            pointer-events: none; z-index: 0;
        }
        .main-wrapper { position: relative; z-index: 1; }

        .app-header { padding: 2.5rem 0 1rem; text-align: center; }
        .app-header .logo-icon {
            display: inline-flex; align-items: center; justify-content: center;
            width: 56px; height: 56px; border-radius: 16px;
            background: var(--accent-dim); border: 1px solid rgba(52,211,153,0.2);
            margin-bottom: 1rem; font-size: 1.4rem; color: var(--accent);
        }
        .app-header h1 {
            font-weight: 700; font-size: 1.75rem;
            letter-spacing: -0.03em; color: var(--text-primary); margin-bottom: 0.35rem;
        }
        .app-header p {
            color: var(--text-secondary); font-size: 0.95rem; font-weight: 400;
            max-width: 480px; margin: 0 auto; line-height: 1.5;
        }

        .process-card {
            background: var(--bg-card); border: 1px solid var(--border-color);
            border-radius: 16px; padding: 2rem; max-width: 600px;
            margin: 1.5rem auto 2rem; transition: border-color 0.3s ease;
        }
        .process-card:hover { border-color: rgba(52,211,153,0.2); }

        .drop-zone {
            border: 2px dashed var(--border-color); border-radius: 12px;
            padding: 2.5rem 1.5rem; text-align: center; cursor: pointer;
            transition: all 0.3s ease; background: transparent; position: relative;
        }
        .drop-zone:hover, .drop-zone.drag-over {
            border-color: var(--accent); background: var(--accent-dim);
        }
        .drop-zone .dz-icon {
            font-size: 2rem; color: var(--text-secondary);
            margin-bottom: 0.75rem; transition: color 0.3s ease;
        }
        .drop-zone:hover .dz-icon, .drop-zone.drag-over .dz-icon { color: var(--accent); }
        .drop-zone .dz-text { color: var(--text-secondary); font-size: 0.9rem; line-height: 1.5; }
        .drop-zone .dz-text strong { color: var(--accent); font-weight: 600; }
        .drop-zone .dz-badge {
            display: inline-block; margin-top: 0.6rem; padding: 0.2rem 0.6rem;
            border-radius: 6px; font-size: 0.72rem; font-weight: 600;
            background: var(--accent-dim); color: var(--accent);
            border: 1px solid rgba(52,211,153,0.15);
        }
        .drop-zone input[type="file"] {
            position: absolute; inset: 0; opacity: 0; cursor: pointer;
        }

        .file-list {
            display: none; margin-top: 1rem; flex-direction: column; gap: 0.4rem;
            max-height: 200px; overflow-y: auto; animation: slideUp 0.3s ease;
        }
        .file-list.visible { display: flex; }
        .file-list::-webkit-scrollbar { width: 5px; }
        .file-list::-webkit-scrollbar-track { background: transparent; }
        .file-list::-webkit-scrollbar-thumb { background: var(--border-color); border-radius: 3px; }

        .file-item {
            display: flex; align-items: center; gap: 0.65rem;
            padding: 0.55rem 0.75rem; background: var(--accent-dim);
            border: 1px solid rgba(52,211,153,0.1); border-radius: 8px; animation: slideUp 0.25s ease;
        }
        .file-item .fi-icon { color: var(--accent); font-size: 0.95rem; flex-shrink: 0; }
        .file-item .fi-name {
            flex: 1; font-family: 'JetBrains Mono', monospace; font-size: 0.78rem;
            color: var(--text-primary); white-space: nowrap; overflow: hidden; text-overflow: ellipsis;
        }
        .file-item .fi-size {
            font-family: 'JetBrains Mono', monospace; font-size: 0.72rem;
            color: var(--text-secondary); flex-shrink: 0;
        }
        .file-item .fi-remove {
            background: none; border: none; color: var(--text-secondary);
            cursor: pointer; padding: 2px 4px; font-size: 0.85rem; transition: color 0.2s; flex-shrink: 0;
        }
        .file-item .fi-remove:hover { color: var(--danger); }

        .file-list-header {
            display: none; align-items: center; justify-content: space-between;
            margin-top: 1rem; padding: 0 0.1rem; animation: slideUp 0.3s ease;
        }
        .file-list-header.visible { display: flex; }
        .file-list-header .flh-label { font-size: 0.8rem; color: var(--text-secondary); font-weight: 500; }
        .file-list-header .flh-count {
            font-family: 'JetBrains Mono', monospace; font-size: 0.75rem;
            color: var(--accent); background: var(--accent-dim); padding: 0.1rem 0.5rem; border-radius: 5px;
        }
        .file-list-header .flh-clear {
            background: none; border: none; color: var(--text-secondary);
            font-size: 0.78rem; cursor: pointer; font-family: 'DM Sans', sans-serif; transition: color 0.2s;
        }
        .file-list-header .flh-clear:hover { color: var(--danger); }

        .btn-process {
            width: 100%; padding: 0.85rem; margin-top: 1.25rem; border: none; border-radius: 10px;
            font-family: 'DM Sans', sans-serif; font-size: 0.95rem; font-weight: 600;
            letter-spacing: -0.01em; cursor: pointer; transition: all 0.25s ease;
            background: var(--accent); color: #0a0f0d; display: flex; align-items: center;
            justify-content: center; gap: 0.5rem;
        }
        .btn-process:hover:not(:disabled) {
            background: #4ade80; box-shadow: 0 0 24px var(--accent-glow); transform: translateY(-1px);
        }
        .btn-process:active:not(:disabled) { transform: translateY(0); }
        .btn-process:disabled { opacity: 0.35; cursor: not-allowed; }
        .btn-process .spinner {
            display: none; width: 18px; height: 18px;
            border: 2px solid rgba(10,15,13,0.3); border-top-color: #0a0f0d;
            border-radius: 50%; animation: spin 0.6s linear infinite;
        }
        .btn-process.loading .spinner { display: block; }
        .btn-process.loading .btn-label { display: none; }

        .msg-alert {
            display: none; align-items: flex-start; gap: 0.65rem; padding: 0.85rem 1rem;
            border-radius: 10px; font-size: 0.88rem; line-height: 1.5; margin-top: 1rem; animation: slideUp 0.3s ease;
        }
        .msg-alert.visible { display: flex; }
        .msg-alert.error { background: var(--danger-dim); border: 1px solid rgba(248,113,113,0.2); color: var(--danger); }
        .msg-alert.warning { background: var(--warning-dim); border: 1px solid rgba(251,191,36,0.2); color: var(--warning); }
        .msg-alert.success { background: var(--accent-dim); border: 1px solid rgba(52,211,153,0.2); color: var(--accent); }
        .msg-alert i { margin-top: 2px; flex-shrink: 0; }

        .results-panel {
            display: none; max-width: 600px; margin: 0 auto 2.5rem; animation: slideUp 0.4s ease;
        }
        .results-panel.visible { display: block; }

        .stats-row { display: grid; grid-template-columns: repeat(4, 1fr); gap: 0.6rem; margin-bottom: 1rem; }
        .stat-box {
            background: var(--bg-card); border: 1px solid var(--border-color);
            border-radius: 12px; padding: 0.85rem 0.5rem; text-align: center;
        }
        .stat-box .stat-value {
            font-family: 'JetBrains Mono', monospace; font-size: 1.35rem; font-weight: 600; color: var(--accent);
        }
        .stat-box .stat-label { font-size: 0.7rem; color: var(--text-secondary); margin-top: 0.15rem; }

        .domain-list {
            background: var(--bg-card); border: 1px solid var(--border-color);
            border-radius: 12px; padding: 0.75rem; margin-bottom: 1rem; max-height: 280px; overflow-y: auto;
        }
        .domain-list::-webkit-scrollbar { width: 6px; }
        .domain-list::-webkit-scrollbar-track { background: transparent; }
        .domain-list::-webkit-scrollbar-thumb { background: var(--border-color); border-radius: 3px; }
        .domain-item {
            display: flex; align-items: center; justify-content: space-between;
            padding: 0.5rem 0.65rem; border-radius: 8px; transition: background 0.2s;
        }
        .domain-item:hover { background: rgba(52,211,153,0.05); }
        .domain-item .di-name { font-family: 'JetBrains Mono', monospace; font-size: 0.82rem; color: var(--text-primary); }
        .domain-item .di-count {
            font-family: 'JetBrains Mono', monospace; font-size: 0.75rem;
            color: var(--text-secondary); background: var(--accent-dim); padding: 0.12rem 0.5rem; border-radius: 6px;
        }

        .btn-download {
            width: 100%; padding: 0.85rem; border: 1px solid var(--accent); border-radius: 10px;
            background: transparent; color: var(--accent); font-family: 'DM Sans', sans-serif;
            font-size: 0.95rem; font-weight: 600; cursor: pointer; transition: all 0.25s ease;
            display: flex; align-items: center; justify-content: center; gap: 0.5rem; text-decoration: none;
        }
        .btn-download:hover {
            background: var(--accent); color: #0a0f0d;
            box-shadow: 0 0 24px var(--accent-glow); transform: translateY(-1px);
        }

        .format-hint { max-width: 600px; margin: 0 auto 3rem; padding: 0 1rem; }
        .format-hint details { background: var(--bg-card); border: 1px solid var(--border-color); border-radius: 12px; overflow: hidden; }
        .format-hint summary {
            padding: 0.85rem 1.1rem; font-size: 0.85rem; color: var(--text-secondary);
            cursor: pointer; list-style: none; display: flex; align-items: center; gap: 0.5rem;
            transition: color 0.2s; user-select: none;
        }
        .format-hint summary:hover { color: var(--text-primary); }
        .format-hint summary::after {
            content: '\f078'; font-family: 'Font Awesome 6 Free'; font-weight: 900;
            font-size: 0.7rem; margin-left: auto; transition: transform 0.2s;
        }
        .format-hint details[open] summary::after { transform: rotate(180deg); }
        .format-hint .hint-body { padding: 0 1.1rem 1rem; border-top: 1px solid var(--border-color); }
        .format-hint pre {
            font-family: 'JetBrains Mono', monospace; font-size: 0.8rem;
            color: var(--text-secondary); margin: 0.75rem 0 0; line-height: 1.7; white-space: pre-wrap;
        }
        .app-footer { text-align: center; padding: 1.5rem 0 2rem; color: var(--text-secondary); font-size: 0.78rem; opacity: 0.6; }

        @keyframes slideUp { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }
        @keyframes spin { to { transform: rotate(360deg); } }
        @media (prefers-reduced-motion: reduce) { *, *::before, *::after { animation-duration: 0.01ms !important; transition-duration: 0.01ms !important; } }
        @media (max-width: 520px) {
            .process-card { margin: 1rem 0.75rem; padding: 1.25rem; }
            .stats-row { grid-template-columns: repeat(2, 1fr); }
            .results-panel { margin: 0 0.75rem 2rem; }
        }
    </style>
</head>
<body>
    <div class="main-wrapper">
        <header class="app-header">
            <div class="logo-icon"><i class="fas fa-layer-group"></i></div>
            <h1>Domain Grouper</h1>
            <p>Upload one or more .txt files with email:password combos — get them all sorted by domain in a single file.</p>
        </header>

        <main>
            <div class="process-card">
                <div class="drop-zone" id="dropZone">
                    <div class="dz-icon"><i class="fas fa-cloud-arrow-up"></i></div>
                    <div class="dz-text">
                        Drag & drop your <strong>.txt</strong> files here<br>
                        or click to browse
                    </div>
                    <div class="dz-badge">MULTIPLE FILES SUPPORTED</div>
                    <input type="file" id="fileInput" accept=".txt" multiple aria-label="Upload text files">
                </div>

                <div class="file-list-header" id="fileListHeader">
                    <span class="flh-label">Selected files</span>
                    <span class="flh-count" id="fileCount">0</span>
                    <button class="flh-clear" id="clearAll">Clear all</button>
                </div>
                <div class="file-list" id="fileList"></div>

                <button class="btn-process" id="btnProcess" disabled>
                    <span class="btn-label"><i class="fas fa-bolt"></i> Process Files</span>
                    <span class="spinner"></span>
                </button>

                <div class="msg-alert error" id="msgError" role="alert">
                    <i class="fas fa-circle-exclamation"></i>
                    <span id="msgErrorText"></span>
                </div>
                <div class="msg-alert warning" id="msgWarning" role="alert">
                    <i class="fas fa-triangle-exclamation"></i>
                    <span id="msgWarningText"></span>
                </div>
                <div class="msg-alert success" id="msgSuccess" role="status">
                    <i class="fas fa-circle-check"></i>
                    <span id="msgSuccessText"></span>
                </div>
            </div>

            <div class="results-panel" id="resultsPanel">
                <div class="stats-row">
                    <div class="stat-box">
                        <div class="stat-value" id="statFiles">0</div>
                        <div class="stat-label">Files</div>
                    </div>
                    <div class="stat-box">
                        <div class="stat-value" id="statTotal">0</div>
                        <div class="stat-label">Total Lines</div>
                    </div>
                    <div class="stat-box">
                        <div class="stat-value" id="statValid">0</div>
                        <div class="stat-label">Valid Entries</div>
                    </div>
                    <div class="stat-box">
                        <div class="stat-value" id="statDomains">0</div>
                        <div class="stat-label">Domains</div>
                    </div>
                </div>
                <div class="domain-list" id="domainList"></div>
                <a href="#" class="btn-download" id="btnDownload" download="finish.txt">
                    <i class="fas fa-download"></i> Download finish.txt
                </a>
            </div>

            <div class="format-hint">
                <details>
                    <summary><i class="fas fa-circle-info"></i> Expected file format</summary>
                    <div class="hint-body">
                        <p style="color:var(--text-secondary);font-size:0.84rem;margin:0.75rem 0 0;">
                            One account per line, email and password separated by a colon:
                        </p>
                        <pre>email@domain.com:password
user@mail.fr:abc123
test@example.org:pass456</pre>
                        <p style="color:var(--text-secondary);font-size:0.84rem;margin:0.5rem 0 0;">
                            You can upload multiple files at once. All entries will be merged and grouped by domain in a single output file.
                        </p>
                    </div>
                </details>
            </div>
        </main>

        <footer class="app-footer">Domain Grouper &mdash; 100% Client-Side. Your files never leave your browser.</footer>
    </div>

    <script>
        const dropZone = document.getElementById('dropZone');
        const fileInput = document.getElementById('fileInput');
        const fileList = document.getElementById('fileList');
        const fileListHeader = document.getElementById('fileListHeader');
        const fileCount = document.getElementById('fileCount');
        const clearAll = document.getElementById('clearAll');
        const btnProcess = document.getElementById('btnProcess');
        const msgError = document.getElementById('msgError');
        const msgErrorText = document.getElementById('msgErrorText');
        const msgWarning = document.getElementById('msgWarning');
        const msgWarningText = document.getElementById('msgWarningText');
        const msgSuccess = document.getElementById('msgSuccess');
        const msgSuccessText = document.getElementById('msgSuccessText');
        const resultsPanel = document.getElementById('resultsPanel');
        const btnDownload = document.getElementById('btnDownload');

        let selectedFiles = [];
        let downloadUrl = null;

        function hideMessages() {
            msgError.classList.remove('visible');
            msgWarning.classList.remove('visible');
            msgSuccess.classList.remove('visible');
        }

        function showError(text) {
            hideMessages();
            msgErrorText.textContent = text;
            msgError.classList.add('visible');
        }

        function showWarning(text) {
            hideMessages();
            msgWarningText.textContent = text;
            msgWarning.classList.add('visible');
        }

        function showSuccess(text) {
            hideMessages();
            msgSuccessText.textContent = text;
            msgSuccess.classList.add('visible');
        }

        function formatSize(bytes) {
            if (bytes < 1024) return bytes + ' B';
            if (bytes < 1024 * 1024) return (bytes / 1024).toFixed(1) + ' KB';
            return (bytes / (1024 * 1024)).toFixed(1) + ' MB';
        }

        function escapeHtml(str) {
            const div = document.createElement('div');
            div.textContent = str;
            return div.innerHTML;
        }

        function renderFileList() {
            fileList.innerHTML = '';
            if (selectedFiles.length === 0) {
                fileList.classList.remove('visible');
                fileListHeader.classList.remove('visible');
                btnProcess.disabled = true;
                return;
            }

            fileListHeader.classList.add('visible');
            fileList.classList.add('visible');
            fileCount.textContent = selectedFiles.length + ' file' + (selectedFiles.length > 1 ? 's' : '');
            btnProcess.disabled = false;

            selectedFiles.forEach((file, index) => {
                const item = document.createElement('div');
                item.className = 'file-item';
                item.innerHTML =
                    '<i class="fas fa-file-lines fi-icon"></i>' +
                    '<span class="fi-name" title="' + escapeHtml(file.name) + '">' + escapeHtml(file.name) + '</span>' +
                    '<span class="fi-size">' + formatSize(file.size) + '</span>' +
                    '<button class="fi-remove" data-index="' + index + '" aria-label="Remove">' +
                    '<i class="fas fa-xmark"></i></button>';
                fileList.appendChild(item);
            });

            fileList.querySelectorAll('.fi-remove').forEach(btn => {
                btn.addEventListener('click', (e) => {
                    selectedFiles.splice(parseInt(e.currentTarget.dataset.index), 1);
                    renderFileList();
                    hideMessages();
                    resultsPanel.classList.remove('visible');
                });
            });
        }

        function addFiles(newFiles) {
            hideMessages();
            resultsPanel.classList.remove('visible');
            let rejected = [];

            for (const file of newFiles) {
                if (!file.name.toLowerCase().endsWith('.txt')) {
                    rejected.push(file.name);
                    continue;
                }
                if (file.size === 0) {
                    rejected.push(file.name + ' (empty)');
                    continue;
                }
                const isDupe = selectedFiles.some(f => f.name === file.name && f.size === file.size);
                if (!isDupe) {
                    selectedFiles.push(file);
                }
            }

            renderFileList();

            if (rejected.length > 0) {
                showError('Skipped: ' + rejected.join(', ') + ' — only non-empty .txt files are accepted.');
            }
        }

        dropZone.addEventListener('dragover', (e) => { e.preventDefault(); dropZone.classList.add('drag-over'); });
        dropZone.addEventListener('dragleave', () => { dropZone.classList.remove('drag-over'); });
        dropZone.addEventListener('drop', (e) => {
            e.preventDefault();
            dropZone.classList.remove('drag-over');
            if (e.dataTransfer.files.length > 0) addFiles(e.dataTransfer.files);
        });

        fileInput.addEventListener('change', () => {
            if (fileInput.files.length > 0) addFiles(fileInput.files);
            fileInput.value = '';
        });

        clearAll.addEventListener('click', () => {
            selectedFiles = [];
            renderFileList();
            hideMessages();
            resultsPanel.classList.remove('visible');
        });

        btnProcess.addEventListener('click', async () => {
            if (selectedFiles.length === 0) return;

            hideMessages();
            resultsPanel.classList.remove('visible');
            btnProcess.classList.add('loading');
            btnProcess.disabled = true;

            try {
                // 1. Read all files text simultaneously
                const readPromises = selectedFiles.map(file => file.text());
                const texts = await Promise.all(readPromises);

                // 2. Extract and clean lines
                let allLines = [];
                texts.forEach(text => {
                    const lines = text.split('\n').map(l => l.trim()).filter(l => l.length > 0);
                    allLines = allLines.concat(lines);
                });

                if (allLines.length === 0) {
                    showError('All uploaded files are empty — no lines to process.');
                    btnProcess.disabled = false;
                    btnProcess.classList.remove('loading');
                    return;
                }

                // 3. Parse and group by domain (Same logic as Python)
                const domains = {};
                let skipped = 0;

                for (const line of allLines) {
                    if (!line.includes(':')) {
                        skipped++;
                        continue;
                    }

                    const parts = line.split(':', 1);
                    const email = parts[0].trim();
                    const password = line.substring(parts[0].length + 1).trim();

                    if (!email || !password) {
                        skipped++;
                        continue;
                    }

                    if (!email.includes('@')) {
                        skipped++;
                        continue;
                    }

                    const domain = email.split('@').pop();
                    
                    if (!domain || !domain.includes('.')) {
                        skipped++;
                        continue;
                    }

                    const fullLine = email + ':' + password;
                    if (!domains[domain]) {
                        domains[domain] = [];
                    }
                    domains[domain].push(fullLine);
                }

                if (Object.keys(domains).length === 0) {
                    showError('No valid email:password entries found in any file. Check the format.');
                    btnProcess.disabled = false;
                    btnProcess.classList.remove('loading');
                    return;
                }

                // 4. Sort domains alphabetically
                const sortedDomains = Object.keys(domains).sort();

                // 5. Build output string
                let outputContent = '';
                sortedDomains.forEach((domain, index) => {
                    outputContent += '##' + domain + '##\n';
                    domains[domain].forEach(entry => {
                        outputContent += entry + '\n';
                    });
                    if (index < sortedDomains.length - 1) {
                        outputContent += '-'.repeat(39) + '\n';
                    }
                });

                // 6. Create downloadable Blob
                if (downloadUrl) {
                    URL.revokeObjectURL(downloadUrl); // Clean up old URL
                }
                const blob = new Blob([outputContent], { type: 'text/plain' });
                downloadUrl = URL.createObjectURL(blob);
                
                btnDownload.href = downloadUrl;

                // 7. Update UI Stats
                const validCount = Object.values(domains).reduce((sum, arr) => sum + arr.length, 0);
                
                document.getElementById('statFiles').textContent = selectedFiles.length;
                document.getElementById('statTotal').textContent = allLines.length;
                document.getElementById('statValid').textContent = validCount;
                document.getElementById('statDomains').textContent = sortedDomains.length;

                const listEl = document.getElementById('domainList');
                listEl.innerHTML = '';
                sortedDomains.forEach(d => {
                    const item = document.createElement('div');
                    item.className = 'domain-item';
                    item.innerHTML = '<span class="di-name">' + escapeHtml(d) + '</span><span class="di-count">' + domains[d].length + '</span>';
                    listEl.appendChild(item);
                });

                let msg = 'Processed ' + validCount + ' entries across ' + sortedDomains.length + ' domains from ' + selectedFiles.length + ' file' + (selectedFiles.length > 1 ? 's' : '') + '.';
                if (skipped > 0) {
                    showWarning(msg + ' (' + skipped + ' invalid lines skipped)');
                } else {
                    showSuccess(msg);
                }

                resultsPanel.classList.add('visible');

            } catch (err) {
                showError('An error occurred while reading the files: ' + err.message);
            }

            btnProcess.disabled = false;
            btnProcess.classList.remove('loading');
        });
    </script>
</body>
</html>
