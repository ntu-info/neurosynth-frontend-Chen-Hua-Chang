<!DOCTYPE html>
<html lang="zh-Hant">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>關鍵字查文獻！</title>
    <!-- 載入 Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* 設定全域字體為 Inter */
        html { font-family: 'Inter', sans-serif; }
        /* 隱藏捲軸但仍可捲動 */
        .no-scrollbar::-webkit-scrollbar { display: none; }
        .no-scrollbar { -ms-overflow-style: none; scrollbar-width: none; }
        /* 自定義樣式 */
        .card {
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -2px rgba(0, 0, 0, 0.06);
        }
        /* 自動完成建議框樣式 */
        .suggestions-box {
            position: absolute;
            width: 100%;
            max-height: 200px;
            overflow-y: auto;
            border: 1px solid #e2e8f0;
            background-color: white;
            z-index: 10;
        }
        .suggestion-item {
            padding: 8px 12px;
            cursor: pointer;
        }
        .suggestion-item:hover {
            background-color: #f1f5f9;
        }
        .suggestion-item strong {
            color: #1d4ed8;
        }

        /* *** 新增：不確定進度條樣式 *** */
        @keyframes indeterminate-progress {
            0% { transform: translateX(-100%); }
            100% { transform: translateX(100%); }
        }
        .progress-bar-indeterminate {
            overflow: hidden;
            background-color: #eef2ff; /* Indigo 50 */
            height: 8px;
            border-radius: 99px;
            position: relative;
        }
        .progress-bar-indeterminate::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            height: 100%;
            width: 60%;
            background-color: #4338ca; /* Indigo 700 */
            border-radius: 99px;
            animation: indeterminate-progress 1.5s ease-in-out infinite;
        }
    </style>
</head>
<body class="bg-gray-50 min-h-screen p-4 sm:p-8">

    <div class="max-w-4xl mx-auto">
        <header class="text-center mb-8">
            <h1 class="text-4xl font-extrabold text-blue-800 mb-2">關鍵字查文獻！d(`･∀･)b</h1>
        </header>

        <!-- API 功能區塊容器 -->
        <div class="space-y-6">

            <!-- 1. 自動載入 - 可用詞彙選單 -->
            <div class="card bg-white p-6 rounded-xl border border-blue-100">
                <h2 class="text-xl font-semibold text-blue-700 mb-4">能用的詞在這裡</h2>
                <p class="text-gray-600 mb-4 font-mono text-sm">GET /terms</p>
                
                <div class="relative mb-4">
                    <label for="termsSearchInput" class="block text-sm font-medium text-gray-700 mb-1">搜尋所有詞彙：</label>
                    <input type="text" id="termsSearchInput" placeholder="在此輸入以篩選下方列表 (e.g., action)" class="w-full p-2 border border-gray-300 rounded-lg focus:ring-blue-500 focus:border-blue-500 transition duration-150">
                    <div id="suggestionsBoxMode1" class="suggestions-box rounded-b-lg shadow-lg hidden"></div>
                </div>

                <div id="termsCloudContainer" class="p-4 bg-gray-50 rounded-lg border border-gray-200 min-h-[50px]">
                    <span id="termsLoadingText" class="text-gray-400">正在載入詞彙列表...</span>
                </div>
            </div>

            <!-- 2. 搜尋介面 (整合功能二與三) -->
            <div class="card bg-white p-6 rounded-xl border border-indigo-100">
                <h2 class="text-xl font-semibold text-indigo-700 mb-4">在這裡搜尋</h2>
                
                <div class="mb-4">
                    <label for="modeSelector" class="block text-sm font-medium text-gray-700 mb-1">選擇搜尋模式：</label>
                    <select id="modeSelector" class="w-full p-2 border border-gray-300 rounded-lg focus:ring-indigo-500 focus:border-indigo-500 transition duration-150">
                        <option value="mode2" selected>查詢相關詞彙</option>
                        <option value="mode3">邏輯搜尋研究</option>
                    </select>
                </div>

                <div id="mode2Wrapper" class="relative">
                    <label for="termInput" class="block text-sm font-medium text-gray-700 mb-1">輸入單一詞彙：</label>
                    <input type="text" id="termInput" placeholder="輸入詞彙 (e.g., amygdala)" class="w-full p-2 border border-gray-300 rounded-lg focus:ring-indigo-500 focus:border-indigo-500 transition duration-150">
                    <div id="suggestionsBoxMode2" class="suggestions-box rounded-b-lg shadow-lg hidden"></div>
                </div>

                <div id="mode3Wrapper" class="hidden">
                    <label class="block text-sm font-medium text-gray-700 mb-1">組合邏輯查詢：</label>
                    <div class="flex flex-col sm:flex-row gap-2">
                        <div class="flex-1 relative">
                            <input type="text" id="term1Input" placeholder="詞彙 1 (e.g., amygdala)" class="w-full p-2 border border-gray-300 rounded-lg focus:ring-green-500 focus:border-green-500 transition duration-150">
                            <div id="suggestionsBoxMode3_1" class="suggestions-box rounded-b-lg shadow-lg hidden"></div>
                        </div>
                        <select id="logicSelector" class="p-2 border border-gray-300 rounded-lg focus:ring-green-500 focus:border-green-500 transition duration-150">
                            <option value="AND">AND</option>
                            <option value="NOT">NOT</option>
                        </select>
                        <div class="flex-1 relative">
                            <input type="text" id="term2Input" placeholder="詞彙 2 (可選, e.g., emotion)" class="w-full p-2 border border-gray-300 rounded-lg focus:ring-green-500 focus:border-green-500 transition duration-150">
                            <div id="suggestionsBoxMode3_2" class="suggestions-box rounded-b-lg shadow-lg hidden"></div>
                        </div>
                    </div>
                </div>

            </div>
        </div>

        <!-- 結果顯示區 -->
        <div id="resultsContainer" class="mt-8">
            <h2 class="text-2xl font-bold text-gray-700 mb-4">查詢結果</h2>
            <!-- *** 修改：更新讀取指示器為進度條 *** -->
            <div id="loadingIndicator" class="hidden p-8 bg-white border border-gray-200 shadow-sm rounded-lg">
                <div class="text-center text-gray-700 font-medium mb-4">
                    正在查詢中...
                </div>
                <div class="w-full progress-bar-indeterminate">
                    <!-- 動畫由 CSS 處理 -->
                </div>
            </div>
            <div id="messageBox" class="p-4 rounded-lg hidden" role="alert"></div>
            <div id="formattedResults" class="mt-4 space-y-4"></div>
        </div>
    </div>

    <script>
        // --- 全域變數 ---
        const BASE_URL = "https://hpc.psy.ntu.edu.tw:5000";
        const DEBOUNCE_TIME = 300; 
        let allTerms = []; 
        let activeSuggestionBox = null; 
        let lastFocusedInput = null; // *** 新增：追蹤最後 focus 的輸入框 ***

        // --- DOM 元素獲取 ---
        const loadingIndicator = document.getElementById('loadingIndicator');
        const messageBox = document.getElementById('messageBox');
        const formattedResults = document.getElementById('formattedResults');
        
        const termsCloudContainer = document.getElementById('termsCloudContainer');
        const termsLoadingText = document.getElementById('termsLoadingText');
        const termsSearchInput = document.getElementById('termsSearchInput'); 

        const modeSelector = document.getElementById('modeSelector');
        const mode2Wrapper = document.getElementById('mode2Wrapper');
        const mode3Wrapper = document.getElementById('mode3Wrapper');
        
        const termInput = document.getElementById('termInput'); // Mode 2
        const term1Input = document.getElementById('term1Input'); // Mode 3
        const logicSelector = document.getElementById('logicSelector'); // Mode 3
        const term2Input = document.getElementById('term2Input'); // Mode 3
        
        const suggestionsBoxMode1 = document.getElementById('suggestionsBoxMode1'); 
        const suggestionsBoxMode2 = document.getElementById('suggestionsBoxMode2');
        const suggestionsBoxMode3_1 = document.getElementById('suggestionsBoxMode3_1');
        const suggestionsBoxMode3_2 = document.getElementById('suggestionsBoxMode3_2');

        // --- 核心輔助函數 (debounce, showMessage, clearResults) ---
        function debounce(func, delay) {
            let timeoutId;
            return function(...args) {
                clearTimeout(timeoutId);
                timeoutId = setTimeout(() => {
                    func.apply(this, args);
                }, delay);
            };
        }

        function showMessage(text, type = 'info') {
            // *** 新增：如果是成功訊息，就不要顯示 ***
            if (type === 'success') {
                messageBox.classList.add('hidden'); // 確保它被隱藏
                return; 
            }
            
            let className = '';
            if (type === 'error') className = 'bg-red-100 text-red-800 border-red-400';
            else if (type === 'success') className = 'bg-green-100 text-green-800 border-green-400';
            else className = 'bg-blue-100 text-blue-800 border-blue-400';
            messageBox.className = `p-4 rounded-lg border ${className} mt-4`;
            messageBox.textContent = text;
            messageBox.classList.remove('hidden');
        }

        function clearResults(clearMessage = true) {
            if (clearMessage) messageBox.classList.add('hidden');
            formattedResults.innerHTML = '';
        }

        /**
         * 處理 API 呼叫的通用函數
         */
        async function fetchAPI(endpoint, queryName) {
            clearResults(false); 
            loadingIndicator.classList.remove('hidden');
            
            const url = `${BASE_URL}${endpoint}`;
            
            try {
                const response = await fetch(url);
                
                if (!response.ok) {
                    const errorText = await response.text();
                    throw new Error(`伺服器回應錯誤: ${response.status} ${response.statusText}`);
                }

                const contentType = response.headers.get('content-type') || '';
                if (contentType.includes('application/json')) {
                    const data = await response.json();
                    showMessage(`✅ ${queryName} 查詢成功! (狀態: ${response.status} ${response.statusText})`, 'success');
                    return data;
                } else {
                    const text = await response.text();
                    showMessage(`⚠️ 成功接收回應 (狀態: ${response.status} ${response.statusText})，但格式非 JSON，無法格式化。`, 'info');
                    return null;
                }
            } catch (err) {
                const errorMessage = err && err.message ? err.message : String(err);
                console.error(`執行 ${queryName} 時發生錯誤:`, err);
                showMessage(`❌ 查詢失敗: ${errorMessage}`, 'error');
                return null;
            } finally {
                loadingIndicator.classList.add('hidden');
            }
        }

        // --- 格式化顯示函數 (displayRelatedTerms, displayStudies) ---

        /**
         * 格式化顯示 - 功能二：相關詞彙
         * (修正：處理物件列表 [object Object] 的問題)
         */
        function displayRelatedTerms(data) {
             const keys = Object.keys(data);
             if (keys.length === 0) {
                 formattedResults.innerHTML = '<p class="text-gray-500">查無相關詞彙。</p>';
                 return;
             }
             const listItems = keys.map(key => {
                 const related = data[key];
                 if (Array.isArray(related)) {
                      // 檢查 'related' 陣列中的項目是否為物件
                      const relatedTermsHtml = related.map(item => {
                          let term = '';
                          let score = '';
                          
                          if (typeof item === 'object' && item !== null && item.term !== undefined) {
                              // 情況 A: 項目是 { term: "...", score: ... }
                              term = item.term;
                              if (item.score !== undefined) {
                                  score = ` (${item.score.toFixed(2)})`;
                              }
                          } else if (typeof item === 'string') {
                              // 情況 B: 項目是簡單字串 (向下相容)
                              term = item;
                          } else {
                              // 情況 C: 未知格式
                              return `<span class="inline-block bg-red-100 text-red-800 text-xs font-medium mr-1 mb-1 px-2 py-0.5 rounded-full">格式錯誤</span>`;
                          }
                          
                          return `<span class="inline-block bg-indigo-100 text-indigo-800 text-xs font-medium mr-1 mb-1 px-2 py-0.5 rounded-full">${term}${score}</span>`;
                      }).join('');

                      return `
                         <li class="p-3 bg-gray-50 rounded-lg border border-gray-200">
                             <strong class="text-indigo-600">${key}:</strong> 
                             <div class="mt-1 flex flex-wrap">${relatedTermsHtml}</div>
                         </li>
                      `;
                 }
                 return '';
             }).join('');
             formattedResults.innerHTML = `
                 <h3 class="text-xl font-medium text-gray-700">相關詞彙細節:</h3>
                 <ul class="space-y-2 list-none p-0">${listItems}</ul>
             `;
        }

        /**
         * 格式化顯示 - 功能三：研究報告
         * (修正：顯示 authors, journal, year 並使用 study_id)
         */
        function displayStudies(studies) {
            if (!Array.isArray(studies) || studies.length === 0) {
                formattedResults.innerHTML = '<p class="text-gray-500">查無文獻。</p>';
                return;
            }

            const studyListItems = studies.map((study) => {
                const title = study.title || '無標題';
                const authors = study.authors || 'N/A';
                const journal = study.journal || 'N/A';
                const year = study.year || 'N/A';
                const pmid = study.study_id || 'N/A'; // (修正：使用 study_id)
                
                return `
                    <li class="p-4 bg-white rounded-lg border border-green-200 hover:shadow-md transition duration-300">
                        <strong class="block text-lg font-semibold text-green-700 mb-1">${title}</strong>
                        <div class="text-sm text-gray-700">
                            <span class="font-medium">作者:</span> ${authors}
                        </div>
                        <div class="text-sm text-gray-500 mt-1">
                            <span class="font-medium">期刊:</span> ${journal} (${year})
                        </div>
                        <div class="mt-2 text-sm text-gray-600">
                            PMID: ${pmid}
                            ${pmid !== 'N/A' ? 
                                `(<a href="https://pubmed.ncbi.nlm.nih.gov/${pmid}" target="_blank" class="text-blue-500 hover:underline">查看 PubMed 原文</a>)` : 
                                ''
                            }
                        </div>
                    </li>
                `;
            }).join('');

            formattedResults.innerHTML = `
                <h3 class="text-xl font-medium text-gray-700">找到 ${studies.length} 份研究報告:</h3>
                <ul class="space-y-3 mt-4">${studyListItems}</ul>
            `;
        }

        // --- 篩選詞彙雲 (功能一) ---
        function filterTermsCloud() {
            const query = termsSearchInput.value.toLowerCase();
            const filteredTerms = query 
                ? allTerms.filter(term => term.toLowerCase().includes(query))
                : allTerms; 

            if (filteredTerms.length > 0) {
                const termHtml = filteredTerms.slice(0, 100).map(term => 
                    `<span class="inline-block bg-blue-100 text-blue-800 text-sm font-medium m-1 px-3 py-1 rounded-full cursor-pointer hover:bg-blue-200 transition duration-150" onclick="selectTerm('${term}')">${term}</span>`
                ).join('');
                termsCloudContainer.innerHTML = termHtml;
            } else {
                termsCloudContainer.innerHTML = '<span class="text-gray-500">未找到符合條件的詞彙。</span>';
            }
        }
        
        // --- 自動完成 (Autocomplete) ---

        function showSuggestions(inputEl, suggestionEl) {
            const query = inputEl.value.toLowerCase();
            if (activeSuggestionBox && activeSuggestionBox !== suggestionEl) {
                activeSuggestionBox.classList.add('hidden');
            }
            
            if (!query || allTerms.length === 0) {
                suggestionEl.classList.add('hidden');
                activeSuggestionBox = null;
                return;
            }

            // *** 修改：實作相關性排序 ***
            const rankedTerms = allTerms.map(term => {
                const lowerTerm = term.toLowerCase();
                let score = 0;
                if (lowerTerm.startsWith(query)) {
                    score = 2; // 開頭符合，最高分
                } else if (lowerTerm.includes(query)) {
                    score = 1; // 包含在內，次高分
                }
                return { term, score };
            })
            .filter(item => item.score > 0) // 只保留有分數的
            .sort((a, b) => b.score - a.score) // 依照分數高低排序
            .slice(0, 10); // 取前 10 名
            
            if (rankedTerms.length === 0) {
                suggestionEl.classList.add('hidden');
                activeSuggestionBox = null;
                return;
            }

            suggestionEl.innerHTML = rankedTerms.map(item => {
                const term = item.term; // 從物件中取出詞彙
                const highlighted = term.replace(new RegExp(query, 'gi'), (match) => `<strong>${match}</strong>`);
                return `<div class="suggestion-item" data-value="${term}">${highlighted}</div>`;
            }).join('');
            // *** 排序邏輯結束 ***

            suggestionEl.classList.remove('hidden');
            activeSuggestionBox = suggestionEl;

            suggestionEl.querySelectorAll('.suggestion-item').forEach(item => {
                item.addEventListener('click', () => {
                    inputEl.value = item.getAttribute('data-value'); 
                    suggestionEl.classList.add('hidden'); 
                    activeSuggestionBox = null;
                    inputEl.dispatchEvent(new Event('input')); 
                });
            });
        }

        function hideAllSuggestions() {
            if (activeSuggestionBox) {
                activeSuggestionBox.classList.add('hidden');
                activeSuggestionBox = null;
            }
        }

        function attachAutocomplete(inputEl, suggestionEl) {
            inputEl.addEventListener('input', () => {
                showSuggestions(inputEl, suggestionEl);
            });
            
            inputEl.addEventListener('blur', () => {
                setTimeout(hideAllSuggestions, 150);
            });
            
            inputEl.addEventListener('focus', () => {
                 showSuggestions(inputEl, suggestionEl);
            });
        }
        
        // --- Live Search 邏輯 ---

        // 功能二：處理 Live Search 相關詞彙
        const handleMode2Search = async () => {
            const term = termInput.value.trim();
            if (!term) {
                clearResults();
                return;
            }
            const endpoint = `/terms/${encodeURIComponent(term)}`;
            const data = await fetchAPI(endpoint, `相關詞彙: ${term}`);
            if (data) { 
                displayRelatedTerms(data); 
            }
        };
        
        // 功能三：處理 Live Search 邏輯搜尋
        // (修正：檢查 data.results 是否存在)
        const handleMode3Search = async () => {
            const term1 = term1Input.value.trim();
            const logic = logicSelector.value;
            const term2 = term2Input.value.trim();

            let queryString = "";

            if (term1 && !term2) {
                queryString = term1;
            } else if (term1 && term2) {
                queryString = `${term1} ${logic} ${term2}`;
            } else {
                clearResults();
                showMessage('請至少在「詞彙 1」中輸入一個詞彙。', 'info');
                return;
            }
            
            const endpoint = `/query/${encodeURIComponent(queryString)}/studies`;
            const data = await fetchAPI(endpoint, `邏輯搜尋: ${queryString}`);
            
            // (修正：API 回傳 { results: [...] } 而非 { studies: [...] })
            if (data && Array.isArray(data.results)) {
                displayStudies(data.results); // 傳入裡面的 results 陣列
            } else if (data) {
                // 雖然成功，但格式不符預期
                console.error("預期 /query 回傳 { results: [...] }，但收到了：", data);
                showMessage("查詢成功，但回傳資料格式不符預期。", "error");
                formattedResults.innerHTML = '<p class="text-gray-500">資料格式錯誤，請檢查主控台。</p>';
            }
            // (如果 data 為 null, fetchAPI 已經顯示了錯誤訊息)
        };

        // --- 應用防抖動 ---
        const debouncedMode2Search = debounce(handleMode2Search, DEBOUNCE_TIME);
        const debouncedMode3Search = debounce(handleMode3Search, DEBOUNCE_TIME);

        // --- 初始化與事件綁定 ---

        // 1. 頁面載入時：自動獲取所有詞彙
        window.addEventListener('load', async () => {
            try {
                const data = await fetch(BASE_URL + '/terms');
                if (!data.ok) throw new Error('伺服器回應錯誤');
                
                const responseData = await data.json(); 
                console.log("從 /terms 獲取的原始資料:", responseData);
                
                if (responseData && Array.isArray(responseData.terms) && responseData.terms.length > 0) {
                    allTerms = responseData.terms; 
                    
                    termsLoadingText.remove(); 
                    filterTermsCloud(); 
                    showMessage(`成功載入 ${allTerms.length} 個詞彙！`, 'success');

                } else if (responseData && Array.isArray(responseData.terms) && responseData.terms.length === 0) {
                    termsLoadingText.textContent = "未找到任何詞彙 (伺服器回傳空列表)。";
                
                } else {
                    termsLoadingText.textContent = "載入失敗：伺服器回傳的資料格式不符預期 (缺少 'terms' 陣列)。";
                    termsLoadingText.classList.add('text-red-600');
                    console.error("預期 /terms 回傳 { terms: [...] }，但收到了：", responseData);
                }
            } catch (err) {
                termsLoadingText.textContent = `載入詞彙失敗: ${err.message}`;
                termsLoadingText.classList.add('text-red-600');
            }
        });

        // *** 修正：點擊詞彙雲中的標籤 ***
        window.selectTerm = (term) => {
            termsSearchInput.value = ''; // 清空功能一的搜尋
            filterTermsCloud(); // 重置詞彙雲

            if (lastFocusedInput) {
                // 如果有紀錄最後點擊的輸入框，就填入該框
                lastFocusedInput.value = term;
                lastFocusedInput.dispatchEvent(new Event('input')); // 觸發 Live Search
            } else {
                // 預設行為：如果使用者還沒點過任何搜尋框，就填入功能二
                modeSelector.value = 'mode2';
                modeSelector.dispatchEvent(new Event('change'));
                termInput.value = term;
                termInput.dispatchEvent(new Event('input')); 
            }
        }

        // 2. 綁定模式切換
        modeSelector.addEventListener('change', () => {
            clearResults();
            if (modeSelector.value === 'mode2') {
                mode2Wrapper.classList.remove('hidden');
                mode3Wrapper.classList.add('hidden');
                termInput.dispatchEvent(new Event('input')); 
            } else {
                mode2Wrapper.classList.add('hidden');
                mode3Wrapper.classList.remove('hidden');
                handleMode3Search(); 
            }
        });

        // 3. 綁定自動完成
        attachAutocomplete(termsSearchInput, suggestionsBoxMode1); 
        attachAutocomplete(termInput, suggestionsBoxMode2);
        attachAutocomplete(term1Input, suggestionsBoxMode3_1);
        attachAutocomplete(term2Input, suggestionsBoxMode3_2);
        
        // *** 新增：追蹤最後一個被 focus 的輸入框 ***
        termInput.addEventListener('focus', (e) => { lastFocusedInput = e.target; });
        term1Input.addEventListener('focus', (e) => { lastFocusedInput = e.target; });
        term2Input.addEventListener('focus', (e) => { lastFocusedInput = e.target; });


        // 4. 綁定 Live Search 觸發器
        termsSearchInput.addEventListener('input', filterTermsCloud); 
        termInput.addEventListener('input', debouncedMode2Search);
        
        term1Input.addEventListener('input', debouncedMode3Search);
        logicSelector.addEventListener('change', debouncedMode3Search);
        term2Input.addEventListener('input', debouncedMode3Search);

        // 5. 點擊頁面其他地方，隱藏建議框
        document.addEventListener('click', (e) => {
            if (!e.target.closest('.relative')) {
                hideAllSuggestions();
            }
        });

    </script>
</body>
</html>



