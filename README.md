<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>🌟 English Funland - Grade 3 Super Review 🌟</title>
    <!-- Google Fonts: Fredoka & Comic Neue for cute 3rd grade vibes -->
    <link href="https://fonts.googleapis.com/css2?family=Comic+Neue:wght@700&family=Fredoka:wght@400;600;700&display=swap" rel="stylesheet">
    <!-- Tailwind CSS for styling -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Canvas Confetti for full-screen celebration explosions -->
    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>
    <style>
        body {
            font-family: 'Fredoka', 'Comic Neue', sans-serif;
            background: linear-gradient(135deg, #ff9a9e 0%, #fad0c4 55%, #ffd1ff 100%);
            min-height: 100vh;
        }
        .cute-shadow {
            box-shadow: 0 8px 0px rgba(0, 0, 0, 0.15), 0 15px 25px rgba(0, 0, 0, 0.1);
        }
        .cute-btn {
            transition: all 0.15s ease-in-out;
        }
        .cute-btn:hover {
            transform: translateY(-3px) scale(1.02);
        }
        .cute-btn:active {
            transform: translateY(2px) scale(0.98);
        }
        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-8px) rotate(2deg); }
        }
        .floating {
            animation: float 3s ease-in-out infinite;
        }
        @keyframes shake {
            0%, 100% { transform: translateX(0); }
            20%, 60% { transform: translateX(-8px); }
            40%, 80% { transform: translateX(8px); }
        }
        .shake-wrong {
            animation: shake 0.4s ease-in-out;
        }
    </style>
</head>
<body class="p-4 md:p-6 text-gray-800">

    <!-- HEADER -->
    <header class="text-center max-w-5xl mx-auto mb-8">
        <div class="inline-block bg-yellow-300 border-4 border-white px-6 py-2 rounded-full cute-shadow mb-3 floating">
            <span class="text-xl md:text-2xl font-bold text-pink-600">✨ Lớp Học Vui Nhộn Của Cô Nancy ✨</span>
        </div>
        <h1 class="text-4xl md:text-6xl font-extrabold text-purple-700 drop-shadow-md mb-2">
            🚀 Grade 3 English Super World 🌟
        </h1>
        <p class="text-lg md:text-xl font-semibold text-white drop-shadow">
            Ôn tập A/An/The, Danh từ số nhiều, Đồ vật, Con vật, Nghề nghiệp & Ghép câu cực vui!
        </p>
    </header>

    <!-- NAVIGATION TABS -->
    <div class="max-w-5xl mx-auto flex flex-wrap justify-center gap-2 md:gap-4 mb-8">
        <button onclick="switchTab('flashcards')" id="tab-flashcards" class="tab-btn px-5 py-3 rounded-2xl font-bold text-base md:text-lg bg-yellow-400 text-purple-900 cute-shadow border-2 border-white transition-all">
            🎒 1. Flashcard Audio
        </button>
        <button onclick="switchTab('plural')" id="tab-plural" class="tab-btn px-5 py-3 rounded-2xl font-bold text-base md:text-lg bg-pink-400 text-white cute-shadow border-2 border-white transition-all">
            ✨ 2. Plural Magic Lab
        </button>
        <button onclick="switchTab('quiz')" id="tab-quiz" class="tab-btn px-5 py-3 rounded-2xl font-bold text-base md:text-lg bg-purple-400 text-white cute-shadow border-2 border-white transition-all">
            🎯 3. Super Quiz Arena
        </button>
        <button onclick="switchTab('story')" id="tab-story" class="tab-btn px-5 py-3 rounded-2xl font-bold text-base md:text-lg bg-green-400 text-white cute-shadow border-2 border-white transition-all">
            📖 4. Story Builder
        </button>
        <button onclick="switchTab('scramble')" id="tab-scramble" class="tab-btn px-5 py-3 rounded-2xl font-bold text-base md:text-lg bg-blue-400 text-white cute-shadow border-2 border-white transition-all">
            🧩 5. Word Scramble
        </button>
        <button onclick="switchTab('sentences')" id="tab-sentences" class="tab-btn px-5 py-3 rounded-2xl font-bold text-base md:text-lg bg-orange-400 text-white cute-shadow border-2 border-white transition-all">
            🗣️ 6. Sentence Master
        </button>
    </div>

    <!-- MAIN CONTAINER -->
    <main class="max-w-5xl mx-auto bg-white/90 backdrop-blur-md rounded-3xl p-6 md:p-10 cute-shadow border-4 border-white mb-12">

        <!-- TAB 1: FLASHCARDS -->
        <section id="content-flashcards" class="tab-content">
            <div class="text-center mb-6">
                <h2 class="text-2xl md:text-3xl font-extrabold text-pink-600 mb-2">🎒 Khám Phá Kho Từ Vựng & Mẫu Câu</h2>
                <p class="text-gray-600">Bấm vào thẻ để nghe phát âm chuẩn bản xứ và xem nghĩa tiếng Việt nhé!</p>
                <div class="flex flex-wrap justify-center gap-2 mt-4">
                    <button onclick="filterVocab('all')" class="px-4 py-1.5 rounded-full bg-purple-200 text-purple-800 font-bold text-sm hover:bg-purple-300">Tất cả</button>
                    <button onclick="filterVocab('objects')" class="px-4 py-1.5 rounded-full bg-yellow-200 text-yellow-800 font-bold text-sm hover:bg-yellow-300">Đồ vật & Nhà cửa</button>
                    <button onclick="filterVocab('animals')" class="px-4 py-1.5 rounded-full bg-green-200 text-green-800 font-bold text-sm hover:bg-green-300">Con vật</button>
                    <button onclick="filterVocab('jobs')" class="px-4 py-1.5 rounded-full bg-pink-200 text-pink-800 font-bold text-sm hover:bg-pink-300">Nghề nghiệp</button>
                    <button onclick="filterVocab('nature')" class="px-4 py-1.5 rounded-full bg-blue-200 text-blue-800 font-bold text-sm hover:bg-blue-300">Tự nhiên & Số đếm</button>
                </div>
            </div>
            <div id="flashcard-grid" class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6">
                <!-- Dynamically rendered by JS -->
            </div>
        </section>

        <!-- TAB 2: PLURAL MAGIC LAB -->
        <section id="content-plural" class="tab-content hidden">
            <div class="text-center mb-6">
                <h2 class="text-2xl md:text-3xl font-extrabold text-purple-600 mb-2">✨ Phòng Thí Nghiệm Danh Từ Số Nhiều (s / es)</h2>
                <p class="text-gray-600">Chọn đúng quy tắc biến đổi số nhiều cho từng từ vựng nhé con!</p>
            </div>
            <div id="plural-game-area" class="max-w-xl mx-auto bg-pink-50 p-6 rounded-3xl border-4 border-pink-200 text-center cute-shadow">
                <!-- Rendered dynamically -->
            </div>
        </section>

        <!-- TAB 3: SUPER QUIZ ARENA -->
        <section id="content-quiz" class="tab-content hidden">
            <div class="text-center mb-6">
                <h2 class="text-2xl md:text-3xl font-extrabold text-indigo-600 mb-2">🎯 Đấu Trường Trắc Nghiệm Thông Minh</h2>
                <p class="text-gray-600">Chọn đáp án đúng nhất với các mẫu câu <i>There is, I have, I can see...</i></p>
            </div>
            <div id="quiz-game-area" class="max-w-xl mx-auto bg-indigo-50 p-6 rounded-3xl border-4 border-indigo-200 cute-shadow">
                <!-- Rendered dynamically -->
            </div>
        </section>

        <!-- TAB 4: STORY BUILDER -->
        <section id="content-story" class="tab-content hidden">
            <div class="text-center mb-6">
                <h2 class="text-2xl md:text-3xl font-extrabold text-green-600 mb-2">📖 Sắp Xếp Câu Chuyện Ngắn</h2>
                <p class="text-gray-600">Sắp xếp các từ xáo trộn để hoàn thành câu chuyện vui nhộn của lớp mình!</p>
            </div>
            <div id="story-game-area" class="max-w-xl mx-auto bg-green-50 p-6 rounded-3xl border-4 border-green-200 cute-shadow text-center">
                <!-- Rendered dynamically -->
            </div>
        </section>

        <!-- TAB 5: WORD SCRAMBLE -->
        <section id="content-scramble" class="tab-content hidden">
            <div class="text-center mb-6">
                <h2 class="text-2xl md:text-3xl font-extrabold text-blue-600 mb-2">🧩 Thử Thách Đánh Vần Từ Vựng</h2>
                <p class="text-gray-600">Bấm vào các chữ cái theo đúng thứ tự để tạo thành từ vựng chính xác!</p>
            </div>
            <div id="scramble-game-area" class="max-w-xl mx-auto bg-blue-50 p-6 rounded-3xl border-4 border-blue-200 cute-shadow text-center">
                <!-- Rendered dynamically -->
            </div>
        </section>

        <!-- TAB 6: SENTENCE MASTER -->
        <section id="content-sentences" class="tab-content hidden">
            <div class="text-center mb-6">
                <h2 class="text-2xl md:text-3xl font-extrabold text-orange-600 mb-2">🗣️ Bậc Thầy Ghép Câu (Sentence Master)</h2>
                <p class="text-gray-600">Lắp ráp các mảnh ghép từ để tạo thành câu hoàn chỉnh đúng ngữ pháp!</p>
            </div>
            <div id="sentence-game-area" class="max-w-xl mx-auto bg-orange-50 p-6 rounded-3xl border-4 border-orange-200 cute-shadow text-center">
                <!-- Rendered dynamically -->
            </div>
        </section>

    </main>

    <!-- FULLSCREEN CELEBRATION MODAL / OVERLAY -->
    <div id="celebration-overlay" class="fixed inset-0 bg-black/60 backdrop-blur-sm z-50 hidden flex items-center justify-center p-4">
        <div id="celebration-box" class="bg-white rounded-3xl p-8 max-w-md w-full text-center cute-shadow border-8 border-yellow-300 transform scale-0 transition-transform duration-300">
            <div class="text-6xl mb-4 floating" id="celebration-emoji">🎉</div>
            <h3 id="celebration-title" class="text-3xl font-extrabold text-pink-600 mb-2">Xuất Sắc Quá Con Ơi!</h3>
            <p id="celebration-desc" class="text-gray-600 text-lg mb-6">Con đã trả lời đúng hoàn toàn câu hỏi này rồi!</p>
            <button onclick="closeCelebration()" class="bg-gradient-to-r from-pink-500 to-yellow-400 text-white font-extrabold px-8 py-3 rounded-full text-lg cute-btn shadow-lg">
                Tiếp Tục Nào! 🚀
            </button>
        </div>
    </div>

    <!-- JAVASCRIPT LOGIC -->
    <script>
        // --- DATABASE VOCABULARY ---
        const vocabularyData = [
            // Objects & House
            { word: "a desk", meaning: "cái bàn học", cat: "objects", emoji: "🪑" },
            { word: "a chair", meaning: "cái ghế", cat: "objects", emoji: "🪑" },
            { word: "a table", meaning: "cái bàn", cat: "objects", emoji: "🪵" },
            { word: "a fridge", meaning: "tủ lạnh", cat: "objects", emoji: "🧊" },
            { word: "a lamp", meaning: "cái đèn", cat: "objects", emoji: "💡" },
            { word: "a cup", meaning: "cái tách, cốc", cat: "objects", emoji: "☕" },
            { word: "a spoon", meaning: "cái muỗng, thìa", cat: "objects", emoji: "🥄" },
            { word: "a fork", meaning: "cái nĩa", cat: "objects", emoji: "🍴" },
            { word: "a piano", meaning: "đàn piano", cat: "objects", emoji: "🎹" },
            { word: "a watch", meaning: "đồng hồ đeo tay", cat: "objects", emoji: "⌚" },
            { word: "a flower", meaning: "bông hoa", cat: "objects", emoji: "🌸" },
            { word: "a book", meaning: "quyển sách", cat: "objects", emoji: "📖" },
            
            // Animals
            { word: "a boy", meaning: "cậu bé", cat: "animals", emoji: "👦" },
            { word: "a zebra", meaning: "con ngựa vằn", cat: "animals", emoji: "🦓" },
            { word: "a bear", meaning: "con gấu", cat: "animals", emoji: "🐻" },
            { word: "an elephant", meaning: "con voi", cat: "animals", emoji: "🐘" },
            { word: "a bird", meaning: "con chim", cat: "animals", emoji: "🐦" },
            { word: "a cow", meaning: "con bò sữa", cat: "animals", emoji: "🐄" },
            { word: "a sheep", meaning: "con cừu", cat: "animals", emoji: "🐑" },
            { word: "a chicken", meaning: "con gà", cat: "animals", emoji: "🐔" },
            { word: "a hen", meaning: "con gà mái", cat: "animals", emoji: "🐓" },
            { word: "a rooster", rating: "gà trống", word: "a rooster", meaning: "con gà trống", cat: "animals", emoji: "🐓" },
            { word: "a rabbit", meaning: "con thỏ", cat: "animals", emoji: "🐰" },

            // Jobs
            { word: "teacher", meaning: "giáo viên", cat: "jobs", emoji: "👩‍🏫" },
            { word: "firefighter", meaning: "lính cứu hỏa", cat: "jobs", emoji: "🚒" },
            { word: "farmer", meaning: "nông dân", cat: "jobs", emoji: "👨‍🌾" },
            { word: "artist", meaning: "họa sĩ, nghệ sĩ", cat: "jobs", emoji: "🎨" },
            { word: "pilot", meaning: "phi công", cat: "jobs", emoji: "✈️" },

            // Nature & Numbers & Fruits (Aha Grammar U1-U3)
            { word: "an apple", meaning: "quả táo", cat: "nature", emoji: "🍎" },
            { word: "an egg", meaning: "quả trứng", cat: "nature", emoji: "🥚" },
            { word: "an orange", meaning: "quả cam", cat: "nature", emoji: "🍊" },
            { word: "an umbrella", meaning: "cái ô, dù", cat: "nature", emoji: "☂️" },
            { word: "an ant", meaning: "con kiến", cat: "nature", emoji: "🐜" },
            { word: "a princess", meaning: "công chúa", cat: "nature", emoji: "👸" },
            { word: "the moon", meaning: "mặt trăng", cat: "nature", emoji: "🌙" },
            { word: "the sun", meaning: "mặt trời", cat: "nature", emoji: "☀️" },
            { word: "the sky", meaning: "bầu trời", cat: "nature", emoji: "☁️" }
        ];

        // Plural Data
        const pluralData = [
            { singular: "boy", plural: "boys", rule: "thêm s", emoji: "👦" },
            { singular: "cookie", plural: "cookies", rule: "thêm s", emoji: "🍪" },
            { singular: "peach", plural: "peaches", rule: "thêm es (ch)", emoji: "🍑" },
            { singular: "bee", plural: "bees", rule: "thêm s", emoji: "🐝" },
            { singular: "watch", plural: "watches", rule: "thêm es (ch)", emoji: "⌚" },
            { singular: "cup", plural: "cups", rule: "thêm s", emoji: "☕" },
            { singular: "dish", plural: "dishes", rule: "thêm es (sh)", emoji: "🍽️" },
            { singular: "fox", plural: "foxes", rule: "thêm es (x)", emoji: "🦊" },
            { singular: "sandwich", plural: "sandwiches", rule: "thêm es (ch)", emoji: "🥪" },
            { singular: "bus", plural: "buses", rule: "thêm es (s)", emoji: "🚌" },
            { singular: "box", plural: "boxes", rule: "thêm es (x)", emoji: "📦" }
        ];

        // Quiz Questions
        const quizData = [
            { q: "Choose the correct article: '... elephant is big.'", options: ["A", "An", "The", "Thes"], answer: "An", explain: "Elephant bắt đầu bằng nguyên âm 'e' nên dùng 'An' con nhé!" },
            { q: "Choose the correct article: '... sun is yellow in the sky.'", options: ["A", "An", "The", "None"], answer: "The", explain: "Mặt trời (sun) là duy nhất nên ta dùng 'The'." },
            { q: "Look and choose: 'There ... a fridge in the kitchen.'", options: ["is", "are", "am", "be"], answer: "is", explain: "'A fridge' là danh từ số ít nên dùng 'There is'." },
            { q: "Plural form of 'watch' is...", options: ["watchs", "watches", "watchies", "watch"], answer: "watches", explain: "Từ tận cùng là 'ch' nên ta phải thêm 'es' thành 'watches'." },
            { q: "Complete the sentence: 'I have ... orange and two apples.'", options: ["a", "an", "the", "two"], answer: "an", explain: "'Orange' bắt đầu bằng 'o' nên dùng 'an'." },
            { q: "What can you see? 'I can see ... fire fighter.'", options: ["a", "an", "the", "two"], answer: "a", explain: "'Firefighter' bắt đầu bằng phụ âm 'f' nên dùng 'a'." }
        ];

        // Stories Data
        const storySentences = [
            { words: ["I", "have", "a", "cute", "rabbit"], correct: "I have a cute rabbit" },
            { words: ["There", "is", "a", "fridge", "in", "the", "kitchen"], correct: "There is a fridge in the kitchen" },
            { words: ["The", "teacher", "is", "happy"], correct: "The teacher is happy" },
            { words: ["I", "can", "see", "two", "foxes"], correct: "I can see two foxes" }
        ];

        // --- AUDIO SPEECH API ---
        function speakText(text) {
            if ('speechSynthesis' in window) {
                window.speechSynthesis.cancel();
                const utterance = new SpeechSynthesisUtterance(text);
                utterance.lang = 'en-US';
                utterance.rate = 0.85; // slightly slower for kids
                window.speechSynthesis.speak(utterance);
            }
        }

        // --- TAB SWITCHER ---
        function switchTab(tabId) {
            document.querySelectorAll('.tab-content').forEach(el => el.classList.add('hidden'));
            document.querySelectorAll('.tab-btn').forEach(btn => {
                btn.classList.remove('bg-yellow-400', 'bg-pink-400', 'bg-purple-400', 'bg-green-400', 'bg-blue-400', 'bg-orange-400', 'scale-105');
                btn.classList.add('bg-gray-200', 'text-gray-700');
            });

            document.getElementById('content-' + tabId).classList.remove('hidden');
            const activeBtn = document.getElementById('tab-' + tabId);
            activeBtn.classList.remove('bg-gray-200', 'text-gray-700');
            
            if(tabId === 'flashcards') activeBtn.classList.add('bg-yellow-400', 'text-purple-900', 'scale-105');
            if(tabId === 'plural') activeBtn.classList.add('bg-pink-400', 'text-white', 'scale-105');
            if(tabId === 'quiz') activeBtn.classList.add('bg-purple-400', 'text-white', 'scale-105');
            if(tabId === 'story') activeBtn.classList.add('bg-green-400', 'text-white', 'scale-105');
            if(tabId === 'scramble') activeBtn.classList.add('bg-blue-400', 'text-white', 'scale-105');
            if(tabId === 'sentences') activeBtn.classList.add('bg-orange-400', 'text-white', 'scale-105');

            if(tabId === 'plural') loadPluralGame();
            if(tabId === 'quiz') loadQuizGame();
            if(tabId === 'story') loadStoryGame();
            if(tabId === 'scramble') loadScrambleGame();
            if(tabId === 'sentences') loadSentenceGame();
        }

        // --- RENDER FLASHCARDS ---
        function renderFlashcards(filter = 'all') {
            const grid = document.getElementById('flashcard-grid');
            grid.innerHTML = '';
            const filtered = filter === 'all' ? vocabularyData : vocabularyData.filter(item => item.cat === filter);

            filtered.forEach(item => {
                const card = document.createElement('div');
                card.className = "bg-gradient-to-br from-yellow-50 to-pink-50 p-6 rounded-3xl border-4 border-white cute-shadow cute-btn cursor-pointer text-center relative overflow-hidden";
                card.onclick = () => {
                    speakText(item.word);
                    card.classList.add('animate-bounce');
                    setTimeout(() => card.classList.remove('animate-bounce'), 600);
                };
                card.innerHTML = `
                    <div class="text-5xl mb-3">${item.emoji}</div>
                    <h3 class="text-2xl font-extrabold text-purple-700 mb-1">${item.word}</h3>
                    <p class="text-gray-600 font-semibold mb-3">${item.meaning}</p>
                    <span class="inline-block bg-pink-500 text-white text-xs font-bold px-3 py-1 rounded-full shadow">🔊 Bấm nghe đọc</span>
                `;
                grid.appendChild(card);
            });
        }

        function filterVocab(cat) {
            renderFlashcards(cat);
        }

        // --- PLURAL GAME LOGIC ---
        let currentPluralIndex = 0;
        function loadPluralGame() {
            currentPluralIndex = Math.floor(Math.random() * pluralData.length);
            const item = pluralData[currentPluralIndex];
            const area = document.getElementById('plural-game-area');

            area.innerHTML = `
                <div class="text-6xl mb-4">${item.emoji}</div>
                <p class="text-gray-500 font-bold mb-1">Danh từ số ít: <span class="text-2xl text-purple-700">${item.singular}</span></p>
                <h3 class="text-3xl font-extrabold text-pink-600 mb-6">Số nhiều của từ này là gì?</h3>
                <div class="grid grid-cols-2 gap-4">
                    <button onclick="checkPlural('${item.singular}s')" class="bg-white border-2 border-pink-300 p-4 rounded-2xl font-extrabold text-xl text-purple-700 cute-btn shadow">${item.singular}s</button>
                    <button onclick="checkPlural('${item.singular}es')" class="bg-white border-2 border-pink-300 p-4 rounded-2xl font-extrabold text-xl text-purple-700 cute-btn shadow">${item.singular}es</button>
                </div>
            `;
        }

        function checkPlural(selected) {
            const item = pluralData[currentPluralIndex];
            const correctPlural = item.plural;
            if(selected === correctPlural || (item.rule.includes('s') && selected === item.plural)) {
                triggerCelebration("Chính Xác Tuyệt Vời! 🌟", `Đúng rồi con ơi, số nhiều của ${item.singular} là ${item.plural}!`);
                speakText("Awesome job!");
                setTimeout(loadPluralGame, 1800);
            } else {
                triggerWrong("Cố Lên Con Cưng! 💪", `Chưa đúng rồi, đáp án đúng phải là ${item.plural} con nhé.`);
                speakText("Try again!");
            }
        }

        // --- QUIZ GAME LOGIC ---
        let currentQuizIndex = 0;
        function loadQuizGame() {
            currentQuizIndex = Math.floor(Math.random() * quizData.length);
            const q = quizData[currentQuizIndex];
            const area = document.getElementById('quiz-game-area');

            let optionsHtml = '';
            q.options.forEach(opt => {
                optionsHtml += `<button onclick="checkQuiz('${opt}', '${q.answer}')" class="bg-white border-2 border-indigo-300 p-4 rounded-2xl font-extrabold text-lg text-indigo-700 cute-btn shadow">${opt}</button>`;
            });

            area.innerHTML = `
                <span class="bg-indigo-200 text-indigo-800 text-xs font-extrabold px-3 py-1 rounded-full uppercase">Câu hỏi trắc nghiệm</span>
                <h3 class="text-xl md:text-2xl font-extrabold text-indigo-900 my-4">${q.q}</h3>
                <div class="grid grid-cols-2 gap-4 mt-4">
                    ${optionsHtml}
                </div>
                <p class="text-xs text-gray-500 mt-4">💡 Mẹo: ${q.explain}</p>
            `;
        }

        function checkQuiz(selected, correct) {
            if(selected === correct) {
                triggerCelebration("Quá Đỉnh Luôn Con Ơi! 🏆", "Con đã chọn đúng đáp án rồi!");
                speakText("Correct!");
                setTimeout(loadQuizGame, 1800);
            } else {
                triggerWrong("Gần Đúng Rồi! 🌈", "Thử suy nghĩ lại một chút nữa xem nào con!");
                speakText("Oops, try again!");
            }
        }

        // --- STORY BUILDER LOGIC ---
        let currentStoryIndex = 0;
        function loadStoryGame() {
            currentStoryIndex = Math.floor(Math.random() * storySentences.length);
            const item = storySentences[currentStoryIndex];
            const shuffled = [...item.words].sort(() => Math.random() - 0.5);
            const area = document.getElementById('story-game-area');

            let wordsHtml = '';
            shuffled.forEach((w, idx) => {
                wordsHtml += `<button onclick="selectStoryWord(this, '${w}')" class="story-word bg-white border-2 border-green-300 px-4 py-2 rounded-xl font-bold text-lg text-green-700 cute-btn shadow m-1">${w}</button>`;
            });

            area.innerHTML = `
                <p class="text-gray-600 font-bold mb-2">Sắp xếp các từ thành câu hoàn chỉnh:</p>
                <div id="story-target" class="min-h-[60px] bg-white border-4 border-dashed border-green-300 rounded-2xl p-3 flex flex-wrap gap-2 items-center justify-center mb-6">
                    <span class="text-gray-400 italic text-sm">Bấm vào các từ bên dưới để xếp vào đây...</span>
                </div>
                <div class="flex flex-wrap justify-center gap-2 mb-6">
                    ${wordsHtml}
                </div>
                <div class="flex justify-center gap-4">
                    <button onclick="checkStory('${item.correct}')" class="bg-green-500 text-white font-extrabold px-6 py-2.5 rounded-full cute-btn shadow">Kiểm Tra ✅</button>
                    <button onclick="loadStoryGame()" class="bg-gray-300 text-gray-700 font-extrabold px-6 py-2.5 rounded-full cute-btn shadow">Đổi Câu 🔄</button>
                </div>
            `;
        }

        let selectedStoryWords = [];
        function selectStoryWord(btn, word) {
            btn.classList.add('hidden');
            selectedStoryWords.push(word);
            updateStoryTarget();
        }

        function updateStoryTarget() {
            const target = document.getElementById('story-target');
            if(selectedStoryWords.length === 0) {
                target.innerHTML = `<span class="text-gray-400 italic text-sm">Bấm vào các từ bên dưới để xếp vào đây...</span>`;
                return;
            }
            target.innerHTML = '';
            selectedStoryWords.forEach((w, idx) => {
                const span = document.createElement('span');
                span.className = "bg-green-100 border border-green-300 px-3 py-1 rounded-lg font-bold text-green-800 text-lg cursor-pointer";
                span.innerText = w;
                span.onclick = () => {
                    selectedStoryWords.splice(idx, 1);
                    loadStoryGame(); // reload to reset
                };
                target.appendChild(span);
            });
        }

        function checkStory(correctSentence) {
            const userSentence = selectedStoryWords.join(' ');
            if(userSentence === correctSentence) {
                triggerCelebration("Ghép Câu Quá Siêu! 🌟", `Chuẩn xác 100%: "${correctSentence}"`);
                speakText(correctSentence);
                setTimeout(loadStoryGame, 2000);
                selectedStoryWords = [];
            } else {
                triggerWrong("Chưa Đúng Rối Con Ơi!", "Thử sắp xếp lại thứ tự từ nhé!");
                speakText("Try again!");
            }
        }

        // --- WORD SCRAMBLE LOGIC ---
        const scrambleWords = [
            { word: "elephant", hint: "Con voi to lớn", emoji: "🐘" },
            { word: "teacher", hint: "Giáo viên", emoji: "👩‍🏫" },
            { word: "fridge", hint: "Tủ lạnh trong bếp", emoji: "🧊" },
            { word: "rabbit", hint: "Con thỏ", emoji: "🐰" },
            { word: "piano", hint: "Đàn piano", emoji: "🎹" },
            { word: "flower", hint: "Bông hoa", emoji: "🌸" }
        ];
        let currentScramble = {};
        let userScrambleLetters = [];

        function loadScrambleGame() {
            currentScramble = scrambleWords[Math.floor(Math.random() * scrambleWords.length)];
            userScrambleLetters = [];
            const letters = currentScramble.word.split('').sort(() => Math.random() - 0.5);
            const area = document.getElementById('scramble-game-area');

            let lettersHtml = '';
            letters.forEach((l, idx) => {
                lettersHtml += `<button onclick="pickScrambleLetter(this, '${l}', ${idx})" class="scramble-btn bg-white border-2 border-blue-300 w-12 h-12 rounded-2xl font-extrabold text-xl text-blue-700 cute-btn shadow m-1">${l}</button>`;
            });

            area.innerHTML = `
                <div class="text-5xl mb-2">${currentScramble.emoji}</div>
                <p class="text-gray-500 font-bold mb-4">Gợi ý: <span class="text-blue-600">${currentScramble.hint}</span></p>
                <div id="scramble-target" class="min-h-[60px] bg-white border-4 border-dashed border-blue-300 rounded-2xl p-3 flex flex-wrap gap-2 items-center justify-center mb-6">
                    <span class="text-gray-400 italic text-sm">Bấm vào các chữ cái bên dưới...</span>
                </div>
                <div class="flex flex-wrap justify-center gap-2 mb-6">
                    ${lettersHtml}
                </div>
                <div class="flex justify-center gap-4">
                    <button onclick="checkScramble()" class="bg-blue-500 text-white font-extrabold px-6 py-2.5 rounded-full cute-btn shadow">Kiểm Tra ✅</button>
                    <button onclick="loadScrambleGame()" class="bg-gray-300 text-gray-700 font-extrabold px-6 py-2.5 rounded-full cute-btn shadow">Đổi Từ 🔄</button>
                </div>
            `;
        }

        function pickScrambleLetter(btn, letter, idx) {
            btn.classList.add('opacity-30', 'pointer-events-none');
            userScrambleLetters.push({ letter, btn });
            updateScrambleTarget();
        }

        function updateScrambleTarget() {
            const target = document.getElementById('scramble-target');
            if(userScrambleLetters.length === 0) {
                target.innerHTML = `<span class="text-gray-400 italic text-sm">Bấm vào các chữ cái bên dưới...</span>`;
                return;
            }
            target.innerHTML = '';
            userScrambleLetters.forEach((item, idx) => {
                const span = document.createElement('span');
                span.className = "bg-blue-100 border border-blue-300 w-10 h-10 rounded-xl font-bold text-blue-800 text-xl flex items-center justify-center cursor-pointer shadow";
                span.innerText = item.letter;
                span.onclick = () => {
                    item.btn.classList.remove('opacity-30', 'pointer-events-none');
                    userScrambleLetters.splice(idx, 1);
                    updateScrambleTarget();
                };
                target.appendChild(span);
            });
        }

        function checkScramble() {
            const formed = userScrambleLetters.map(i => i.letter).join('');
            if(formed === currentScramble.word) {
                triggerCelebration("Giải Đố Quá Siêu! 🌟", `Chính xác từ "${currentScramble.word}" rồi con ơi!`);
                speakText(currentScramble.word);
                setTimeout(loadScrambleGame, 2000);
            } else {
                triggerWrong("Chưa Đúng Rồi!", "Thử xóa đi xếp lại xem nào con!");
                speakText("Try again!");
            }
        }

        // --- SENTENCE MASTER LOGIC ---
        const sentenceList = [
            { scrambled: ["There", "is", "a", "flower", "on", "the", "desk"], correct: "There is a flower on the desk" },
            { scrambled: ["I", "have", "two", "cute", "dogs"], correct: "I have two cute dogs" },
            { scrambled: ["I", "can", "see", "an", "elephant"], correct: "I can see an elephant" },
            { scrambled: ["The", "sun", "is", "in", "the", "sky"], correct: "The sun is the sky" }
        ];
        let currentSentMaster = {};
        let userSentWords = [];

        function loadSentenceGame() {
            currentSentMaster = sentenceList[Math.floor(Math.random() * sentenceList.length)];
            userSentWords = [];
            const shuffled = [...currentSentMaster.scrambled].sort(() => Math.random() - 0.5);
            const area = document.getElementById('sentence-game-area');

            let wordsHtml = '';
            shuffled.forEach((w, idx) => {
                wordsHtml += `<button onclick="pickSentWord(this, '${w}')" class="sent-btn bg-white border-2 border-orange-300 px-4 py-2 rounded-xl font-bold text-lg text-orange-700 cute-btn shadow m-1">${w}</button>`;
            });

            area.innerHTML = `
                <p class="text-gray-600 font-bold mb-2">Lắp ráp thành câu hoàn chỉnh đúng ngữ pháp:</p>
                <div id="sent-target" class="min-h-[60px] bg-white border-4 border-dashed border-orange-300 rounded-2xl p-3 flex flex-wrap gap-2 items-center justify-center mb-6">
                    <span class="text-gray-400 italic text-sm">Bấm vào các từ bên dưới...</span>
                </div>
                <div class="flex flex-wrap justify-center gap-2 mb-6">
                    ${wordsHtml}
                </div>
                <div class="flex justify-center gap-4">
                    <button onclick="checkSentenceMaster()" class="bg-orange-500 text-white font-extrabold px-6 py-2.5 rounded-full cute-btn shadow">Kiểm Tra ✅</button>
                    <button onclick="loadSentenceGame()" class="bg-gray-300 text-gray-700 font-extrabold px-6 py-2.5 rounded-full cute-btn shadow">Đổi Câu 🔄</button>
                </div>
            `;
        }

        function pickSentWord(btn, word) {
            btn.classList.add('opacity-30', 'pointer-events-none');
            userSentWords.push({ word, btn });
            updateSentTarget();
        }

        function updateSentTarget() {
            const target = document.getElementById('sent-target');
            if(userSentWords.length === 0) {
                target.innerHTML = `<span class="text-gray-400 italic text-sm">Bấm vào các từ bên dưới...</span>`;
                return;
            }
            target.innerHTML = '';
            userSentWords.forEach((item, idx) => {
                const span = document.createElement('span');
                span.className = "bg-orange-100 border border-orange-300 px-3 py-1 rounded-lg font-bold text-orange-800 text-lg cursor-pointer shadow";
                span.innerText = item.word;
                span.onclick = () => {
                    item.btn.classList.remove('opacity-30', 'pointer-events-none');
                    userSentWords.splice(idx, 1);
                    updateSentTarget();
                };
                target.appendChild(span);
            });
        }

        function checkSentenceMaster() {
            const formed = userSentWords.map(i => i.word).join(' ');
            if(formed === currentSentMaster.correct) {
                triggerCelebration("Giỏi Quá Con Ơi! 🌟", `Câu hoàn chỉnh: "${currentSentMaster.correct}"`);
                speakText(currentSentMaster.correct);
                setTimeout(loadSentenceGame, 2000);
            } else {
                triggerWrong("Chưa Đúng Ngữ Pháp Rồi!", "Con hãy kiểm tra lại vị trí các từ nhé!");
                speakText("Try again!");
            }
        }

        // --- CELEBRATION & ERROR EFFECTS ---
        function triggerCelebration(title, desc) {
            // Fullscreen Confetti Explosion
            confetti({
                particleCount: 120,
                spread: 90,
                origin: { y: 0.6 }
            });

            const overlay = document.getElementById('celebration-overlay');
            const box = document.getElementById('celebration-box');
            document.getElementById('celebration-title').innerText = title;
            document.getElementById('celebration-desc').innerText = desc;
            document.getElementById('celebration-emoji').innerText = "🌟🎉🏆";

            overlay.classList.remove('hidden');
            setTimeout(() => {
                box.classList.remove('scale-0');
                box.classList.add('scale-100');
            }, 50);
        }

        function triggerWrong(title, desc) {
            const overlay = document.getElementById('celebration-overlay');
            const box = document.getElementById('celebration-box');
            document.getElementById('celebration-title').innerText = title;
            document.getElementById('celebration-desc').innerText = desc;
            document.getElementById('celebration-emoji').innerText = "💪🌈";

            overlay.classList.remove('hidden');
            setTimeout(() => {
                box.classList.remove('scale-0');
                box.classList.add('scale-100');
                box.classList.add('shake-wrong');
            }, 50);
            setTimeout(() => {
                box.classList.remove('shake-wrong');
            }, 500);
        }

        function closeCelebration() {
            const overlay = document.getElementById('celebration-overlay');
            const box = document.getElementById('celebration-box');
            box.classList.remove('scale-100');
            box.classList.add('scale-0');
            setTimeout(() => {
                overlay.classList.add('hidden');
            }, 300);
        }

        // Initialize First Tab
        renderFlashcards();
    </script>
</body>
</html>
