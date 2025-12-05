<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Online Calculator, BMI, Currency Converter - Utility Nexus</title>
    <meta name="description" content="Utility Nexus provides a fast, all-in-one suite of online tools: Scientific Calculator, Body Mass Index (BMI) calculator, and an essential Currency Converter. Mobile-friendly and ready for daily use.">
    <!-- Tailwind CSS (For great mobile-first styling) -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;800&display=swap');
        body { font-family: 'Inter', sans-serif; background-color: #f7f7f9; }
        .tab-content { display: none; }
        .tab-content.active { display: block; }
        .calc-btn { transition: background-color 0.1s; }
        .calc-btn:active { transform: scale(0.98); }
        .page-content { display: none; } /* For Contact and Privacy Pages */
        .page-content:target { display: block; } /* Show based on URL fragment */
    </style>
</head>
<body class="min-h-screen flex flex-col">

    <!-- Header and Navigation -->
    <header class="bg-white shadow-md p-4 sticky top-0 z-10">
        <div class="max-w-6xl mx-auto flex justify-between items-center">
            <h1 class="text-2xl font-extrabold text-blue-700">Utility Nexus</h1>
            <!-- Links using fragment identifiers for single file structure -->
            <nav class="space-x-4">
                <a href="#home" class="text-blue-500 font-semibold hover:text-blue-700">Home</a>
                <a href="#privacy" class="text-gray-600 hover:text-blue-700">Privacy Policy</a>
                <a href="#contact" class="text-gray-600 hover:text-blue-700">Contact Us</a>
            </nav>
        </div>
    </header>

    <!-- Main Tool Content Area (Targeted by #home) -->
    <main id="home" class="flex-grow max-w-4xl mx-auto p-4 md:p-8 w-full page-content active">
        
        <h2 class="text-3xl md:text-4xl font-extrabold text-gray-800 text-center mb-6">Free Online Utility Tools (Calc, BMI, Currency)</h2>
        
        <!-- Ad Slot 1 (Top Banner) - AdSense Code Here -->
        <div id="ad-slot-1" class="my-6 p-3 bg-red-100 border border-red-300 text-center text-red-700 rounded-lg font-mono text-sm">
            <!-- APNA PEHLA RESPONSIVE AD SENSE CODE YAHAN PASTE KAREIN -->
            Advertisement Slot 1 (For AdSense Approval)
        </div>

        <!-- Tool Tabs -->
        <div class="flex justify-center mb-6 bg-white p-2 rounded-xl shadow-lg">
            <button id="tab-calculator-btn" class="tab-button flex-1 py-3 px-2 text-sm md:text-base font-semibold rounded-lg transition-all bg-blue-600 text-white shadow-md" data-tab="calculator">Calculator</button>
            <button id="tab-bmi-btn" class="tab-button flex-1 py-3 px-2 text-sm md:text-base font-semibold rounded-lg transition-all text-gray-700 hover:bg-gray-100" data-tab="bmi">BMI</button>
            <button id="tab-currency-btn" class="tab-button flex-1 py-3 px-2 text-sm md:text-base font-semibold rounded-lg transition-all text-gray-700 hover:bg-gray-100" data-tab="currency">Currency</button>
        </div>

        <!-- CALCULATOR Tab Content -->
        <div id="calculator" class="tab-content active bg-white shadow-xl rounded-xl p-6 md:p-8">
            <h3 class="text-2xl font-bold text-gray-700 mb-4 text-center">Scientific Calculator</h3>
            <div class="calculator-body bg-gray-100 p-4 rounded-lg shadow-inner">
                <input type="text" id="calc-display" class="w-full h-16 mb-4 p-3 text-3xl text-right border-2 border-gray-300 rounded-lg font-mono bg-white shadow-md focus:outline-none" value="0" disabled>
                
                <div class="grid grid-cols-4 gap-2">
                    <!-- Calculator buttons code remains the same -->
                    <button class="calc-btn bg-red-500 hover:bg-red-600 text-white p-4 rounded-lg font-bold text-xl" data-action="clear">AC</button>
                    <button class="calc-btn bg-gray-400 hover:bg-gray-500 text-white p-4 rounded-lg font-bold text-xl" data-action="operator" data-value="%">%</button>
                    <button class="calc-btn bg-gray-400 hover:bg-gray-500 text-white p-4 rounded-lg font-bold text-xl" data-action="operator" data-value="/">÷</button>
                    <button class="calc-btn bg-blue-500 hover:bg-blue-600 text-white p-4 rounded-lg font-bold text-xl" data-action="operator" data-value="*">×</button>
                    
                    <button class="calc-btn bg-gray-200 hover:bg-gray-300 p-4 rounded-lg font-bold text-xl" data-action="number" data-value="7">7</button>
                    <button class="calc-btn bg-gray-200 hover:bg-gray-300 p-4 rounded-lg font-bold text-xl" data-action="number" data-value="8">8</button>
                    <button class="calc-btn bg-gray-200 hover:bg-gray-300 p-4 rounded-lg font-bold text-xl" data-action="number" data-value="9">9</button>
                    <button class="calc-btn bg-blue-500 hover:bg-blue-600 text-white p-4 rounded-lg font-bold text-xl" data-action="operator" data-value="-">-</button>
                    
                    <button class="calc-btn bg-gray-200 hover:bg-gray-300 p-4 rounded-lg font-bold text-xl" data-action="number" data-value="4">4</button>
                    <button class="calc-btn bg-gray-200 hover:bg-gray-300 p-4 rounded-lg font-bold text-xl" data-action="number" data-value="5">5</button>
                    <button class="calc-btn bg-gray-200 hover:bg-gray-300 p-4 rounded-lg font-bold text-xl" data-action="number" data-value="6">6</button>
                    <button class="calc-btn bg-blue-500 hover:bg-blue-600 text-white p-4 rounded-lg font-bold text-xl" data-action="operator" data-value="+">+</button>
                    
                    <button class="calc-btn bg-gray-200 hover:bg-gray-300 p-4 rounded-lg font-bold text-xl" data-action="number" data-value="1">1</button>
                    <button class="calc-btn bg-gray-200 hover:bg-gray-300 p-4 rounded-lg font-bold text-xl" data-action="number" data-value="2">2</button>
                    <button class="calc-btn bg-gray-200 hover:bg-gray-300 p-4 rounded-lg font-bold text-xl" data-action="number" data-value="3">3</button>
                    <button class="calc-btn bg-green-500 hover:bg-green-600 text-white p-4 rounded-lg font-bold text-xl row-span-2" data-action="calculate">=</button>
                    
                    <button class="calc-btn bg-gray-200 hover:bg-gray-300 p-4 rounded-lg font-bold text-xl col-span-2" data-action="number" data-value="0">0</button>
                    <button class="calc-btn bg-gray-200 hover:bg-gray-300 p-4 rounded-lg font-bold text-xl" data-action="decimal" data-value=".">.</button>
                </div>
            </div>
        </div>

        <!-- BMI Tab Content -->
        <div id="bmi" class="tab-content bg-white shadow-xl rounded-xl p-6 md:p-8">
            <h3 class="text-2xl font-bold text-gray-700 mb-4 text-center">Body Mass Index (BMI) Calculator</h3>
            <div class="space-y-4">
                <label for="weight" class="block text-lg font-medium text-gray-700">Weight (Kilograms):</label>
                <input type="number" id="weight" class="w-full p-3 border border-gray-300 rounded-lg focus:ring-blue-500 focus:border-blue-500" placeholder="e.g., 70" min="1" required>
                
                <label for="height" class="block text-lg font-medium text-gray-700">Height (Meters):</label>
                <input type="number" id="height" class="w-full p-3 border border-gray-300 rounded-lg focus:ring-blue-500 focus:border-blue-500" placeholder="e.g., 1.75" min="0.1" step="0.01" required>

                <button id="calculate-bmi" class="w-full py-3 bg-green-600 text-white font-semibold rounded-lg hover:bg-green-700 transition">Calculate BMI</button>
            </div>
            <div id="bmi-result" class="mt-6 p-4 bg-blue-50 border border-blue-200 rounded-lg text-center hidden">
                <p class="text-xl font-bold text-gray-800">Your BMI: <span id="bmi-value" class="text-blue-700"></span></p>
                <p class="text-lg mt-2 text-gray-600">Status: <span id="bmi-status" class="font-semibold"></span></p>
            </div>
            <div id="bmi-error" class="mt-4 p-3 bg-red-100 text-red-700 rounded-lg hidden">Please enter valid weight and height values.</div>
        </div>

        <!-- CURRENCY Tab Content (PKR aur BHD ke saath updated) -->
        <div id="currency" class="tab-content bg-white shadow-xl rounded-xl p-6 md:p-8">
            <h3 class="text-2xl font-bold text-gray-700 mb-4 text-center">Currency Converter (Sample Rates)</h3>
            <p class="text-sm text-center text-red-500 mb-4">Note: This converter uses static sample rates for demonstration and quick estimation. For live transaction rates, please consult a financial institution.</p>
            <div class="space-y-4">
                <div>
                    <label for="amount" class="block text-lg font-medium text-gray-700">Amount:</label>
                    <input type="number" id="amount" class="w-full p-3 border border-gray-300 rounded-lg focus:ring-blue-500 focus:border-blue-500" placeholder="Enter amount" value="100" min="0">
                </div>
                
                <div class="flex space-x-4">
                    <div class="flex-1">
                        <label for="from-currency" class="block text-lg font-medium text-gray-700">From:</label>
                        <select id="from-currency" class="w-full p-3 border border-gray-300 rounded-lg focus:ring-blue-500 focus:border-blue-500">
                            <!-- New Currencies Added -->
                            <option value="USD">USD - US Dollar</option>
                            <option value="EUR">EUR - Euro</option>
                            <option value="INR" selected>INR - Indian Rupee</option>
                            <option value="PKR">PKR - Pakistani Rupee</option>
                            <option value="BHD">BHD - Bahraini Dinar</option>
                            <option value="GBP">GBP - British Pound</option>
                            <option value="JPY">JPY - Japanese Yen</option>
                        </select>
                    </div>
                    <div class="flex-1">
                        <label for="to-currency" class="block text-lg font-medium text-gray-700">To:</label>
                        <select id="to-currency" class="w-full p-3 border border-gray-300 rounded-lg focus:ring-blue-500 focus:border-blue-500">
                            <!-- New Currencies Added -->
                            <option value="USD" selected>USD - US Dollar</option>
                            <option value="EUR">EUR - Euro</option>
                            <option value="INR">INR - Indian Rupee</option>
                            <option value="PKR">PKR - Pakistani Rupee</option>
                            <option value="BHD">BHD - Bahraini Dinar</option>
                            <option value="GBP">GBP - British Pound</option>
                            <option value="JPY">JPY - Japanese Yen</option>
                        </select>
                    </div>
                </div>

                <button id="convert-currency" class="w-full py-3 bg-blue-600 text-white font-semibold rounded-lg hover:bg-blue-700 transition">Convert</button>
            </div>
            <div id="conversion-result" class="mt-6 p-4 bg-green-50 border border-green-200 rounded-lg text-center hidden">
                <p class="text-xl font-bold text-gray-800">Result: <span id="converted-value" class="text-green-700"></span></p>
                <p class="text-sm mt-2 text-gray-500">Based on sample exchange rates.</p>
            </div>
        </div>

        <!-- Ad Slot 2 (Mid Content) - AdSense Code Here -->
        <div id="ad-slot-2" class="my-10 p-4 bg-yellow-100 border border-yellow-300 text-center text-yellow-800 rounded-lg font-mono text-sm">
            <!-- APNA DOOSRA RESPONSIVE AD SENSE CODE YAHAN PASTE KAREIN -->
            Advertisement Slot 2 (For AdSense Approval)
        </div>

        <!-- AdSense Required SEO Content (200 words approx) -->
        <div class="mt-12 space-y-8 p-4 border-t border-gray-200">
            
            <section>
                <h2 class="text-2xl font-bold text-gray-700 border-b pb-2 mb-4">What is a Modern Web Calculator?</h2>
                <p class="text-gray-600 leading-relaxed">
                    A calculator is an essential digital tool designed to perform mathematical operations, ranging from simple arithmetic (addition, subtraction, multiplication, division) to more complex scientific functions. This modern web-based calculator provides instant and accurate results for everyday calculations. Unlike physical calculators, our online tool is accessible on any device, ensuring you can quickly solve problems whether you are at home, in the office, or studying.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-700 border-b pb-2 mb-4">Understanding BMI and Currency Conversion</h2>
                <p class="text-gray-600 leading-relaxed">
                    The Body Mass Index (BMI) is a health measure that uses your weight and height to estimate if you are underweight, at a healthy weight, overweight, or obese. It is a simple screening tool to identify potential weight problems. Similarly, the Currency Converter provides essential financial information, allowing users to estimate the value of one currency in terms of another. This is crucial for international business, travel planning, or cross-border e-commerce transactions, offering instant access to current sample exchange rates for quick financial estimates.
                </p>
            </section>
        </div>
        <!-- END AdSense Required SEO Content -->
    </main>

    <!-- Zaroori Page Content Sections (Hidden by default, shown via anchor link) -->

    <!-- PRIVACY POLICY SECTION (Targeted by #privacy) -->
    <section id="privacy" class="page-content max-w-4xl mx-auto p-4 md:p-8 w-full">
        <div class="bg-white shadow-xl rounded-xl p-8 md:p-12">
            <h1 class="text-4xl font-extrabold text-blue-700 mb-6 border-b pb-2 text-center">Privacy Policy (Utility Nexus)</h1>
            
            <p class="mb-4 text-gray-600">
                Utility Nexus (Humari Site) ko istemaal karne ke liye hum aapki privacy ka samman karte hain. Yeh document batata hai ki hum kaunsi jankari (information) collect karte hain aur uska istemaal kaise karte hain.
            </p>

            <h2 class="text-2xl font-bold text-gray-700 mt-6 border-b pb-2">1. Data Collection</h2>
            <p class="text-gray-600 mt-2">
                Humari site par koi bhi **vyaktigat (personal)** jankari automatic taur par collect nahi ki jaati hai. Aapke calculator ke inputs, BMI values, ya currency conversion data humare servers par **store nahi** hote hain. Yeh sab calculation aapke browser (local device) mein hi hoti hai.
            </p>
            <ul class="list-disc list-inside ml-4 text-gray-600 mt-3 space-y-1">
                <li>**Zaroori Input:** Aap jo numbers ya values tools mein daalte hain, woh humari pahunch se bahar rehte hain.</li>
                <li>**Contact Data:** Agar aap humein 'Contact Us' page se email bhejte hain, toh hum sirf us email address ka istemaal aapko jawab dene ke liye karte hain.</li>
            </ul>

            <h2 class="text-2xl font-bold text-gray-700 mt-6 border-b pb-2">2. Cookies aur Tracking Technologies</h2>
            <p class="text-gray-600 mt-2">
                Humari site khud koi primary tracking cookies istemaal nahi karti. Lekin hum third-party services, jaise **Google AdSense** ka upyog karte hain vigyapan (advertisements) dikhane ke liye.
            </p>
            <ul class="list-disc list-inside ml-4 text-gray-600 mt-3 space-y-1">
                <li>**Google AdSense:** Google AdSense aapki browsing history ke aadhar par aapko relevant ads dikhane ke liye cookies ka istemaal karta hai.</li>
                <li>**DART Cookie:** Google DART cookies ka upyog karta hai taaki aapko doosri sites par jaate waqt bhi ads dikhayein jo aapki ruchi (interest) ke hisaab se ho.</li>
                <li>Aap Google ke Ad Network aur Content Network privacy policy ko padh kar DART cookies ke istemaal se inkar (opt-out) kar sakte hain.</li>
            </ul>
            
            <h2 class="text-2xl font-bold text-gray-700 mt-6 border-b pb-2">3. Consent</h2>
            <p class="text-gray-600 mt-2">
                Humari site ka upyog karke, aap humari Privacy Policy se sehma hain aur iski terms ko sweekar karte hain.
            </p>

            <a href="#home" class="mt-8 inline-block px-6 py-3 bg-blue-500 text-white font-semibold rounded-lg hover:bg-blue-600 transition">Go Back to Home</a>
        </div>
    </section>

    <!-- CONTACT US SECTION (Targeted by #contact) -->
    <section id="contact" class="page-content max-w-4xl mx-auto p-4 md:p-8 w-full">
        <div class="bg-white shadow-xl rounded-xl p-8 md:p-12 text-center">
            <h1 class="text-4xl font-extrabold text-blue-700 mb-6 border-b pb-2">Humse Sampark Karein (Contact Us)</h1>
            
            <p class="mb-6 text-lg text-gray-600">Agar aapke paas humare tools ke baare mein koi sawaal, sujhav, ya takneeki (technical) samasya hai, toh aap humse sampark kar sakte hain.</p>

            <div class="p-6 bg-blue-50 border border-blue-200 rounded-lg inline-block">
                <h2 class="text-2xl font-bold text-gray-800 mb-3">Email Address</h2>
                <p class="text-xl font-mono text-blue-700 break-all">
                    <a href="mailto:nomimalik554@gmail.com" class="hover:underline">nomimalik554@gmail.com</a>
                </p>
                <p class="mt-2 text-sm text-gray-500">Hum koshish karte hain ki 24-48 ghante ke bheetar jawab dein.</p>
            </div>

            <a href="#home" class="mt-10 inline-block px-6 py-3 bg-blue-500 text-white font-semibold rounded-lg hover:bg-blue-600 transition">Go Back to Home</a>
        </div>
    </section>
    
    <!-- Footer -->
    <footer class="bg-gray-800 text-white p-6 mt-8">
        <div class="max-w-6xl mx-auto text-center">
            <p class="text-lg font-semibold mb-2">Utility Nexus</p>
            <nav class="space-x-4 text-sm mb-4">
                <a href="#home" class="hover:underline">Home</a>
                <a href="#privacy" class="hover:underline">Privacy Policy</a>
                <a href="#contact" class="hover:underline">Contact Us</a>
            </nav>
            <p class="text-xs text-gray-400">&copy; 2025 Utility Nexus. All rights reserved. Designed for speed and compliance.</p>
        </div>
    </footer>


    <script>
        // --- Single File Navigation Logic ---
        function navigateTo(hash) {
            // Hide all content sections
            document.querySelectorAll('.page-content').forEach(section => {
                section.style.display = 'none';
                section.classList.remove('active');
            });

            // Show the target section
            const targetSection = document.querySelector(hash);
            if (targetSection) {
                targetSection.style.display = 'block';
                targetSection.classList.add('active');
            }
            
            // If navigating to home, ensure the calculator tab is visible
            if (hash === '#home') {
                document.getElementById('calculator').style.display = 'block'; 
                document.getElementById('calculator').classList.add('active'); 
            }
        }

        // Handle initial load and hash changes
        window.addEventListener('hashchange', () => navigateTo(window.location.hash || '#home'));
        window.addEventListener('DOMContentLoaded', () => navigateTo(window.location.hash || '#home'));

        // Attach event listeners to all internal links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const hash = this.getAttribute('href');
                window.location.hash = hash;
                // navigateTo will be called by the hashchange listener, but we call it here for instant feedback
                navigateTo(hash);
            });
        });


        // --- Tool Tab Switching Logic ---
        document.querySelectorAll('.tab-button').forEach(button => {
            button.addEventListener('click', function() {
                // Remove active class from all buttons and content
                document.querySelectorAll('.tab-button').forEach(btn => {
                    btn.classList.remove('bg-blue-600', 'text-white', 'shadow-md');
                    btn.classList.add('text-gray-700', 'hover:bg-gray-100');
                });
                document.querySelectorAll('.tab-content').forEach(content => {
                    content.classList.remove('active');
                    content.style.display = 'none'; // Ensure CSS display property is explicitly set
                });

                // Add active class to the clicked button and corresponding content
                this.classList.add('bg-blue-600', 'text-white', 'shadow-md');
                this.classList.remove('text-gray-700', 'hover:bg-gray-100');
                
                const targetId = this.getAttribute('data-tab');
                const targetContent = document.getElementById(targetId);
                targetContent.classList.add('active');
                targetContent.style.display = 'block'; // Show the content
            });
        });
        // Initial setup for tool tabs (only run if on #home)
        if (window.location.hash === '' || window.location.hash === '#home') {
            document.addEventListener('DOMContentLoaded', () => {
                document.getElementById('calculator').style.display = 'block'; 
            });
        }


        // --- Calculator Logic (Same as before) ---
        const display = document.getElementById('calc-display');
        let currentInput = '0';
        let operator = null;
        let previousInput = null;
        let waitingForSecondOperand = false;

        function updateDisplay() {
            display.value = currentInput;
        }

        function clear() {
            currentInput = '0';
            operator = null;
            previousInput = null;
            waitingForSecondOperand = false;
        }

        function inputNumber(number) {
            if (waitingForSecondOperand) {
                currentInput = number;
                waitingForSecondOperand = false;
            } else {
                currentInput = currentInput === '0' ? number : currentInput + number;
            }
            updateDisplay();
        }

        function inputDecimal() {
            if (waitingForSecondOperand) {
                currentInput = '0.';
                waitingForSecondOperand = false;
                return;
            }
            if (!currentInput.includes('.')) {
                currentInput += '.';
            }
            updateDisplay();
        }

        function handleOperator(nextOperator) {
            const inputValue = parseFloat(currentInput);

            if (operator && waitingForSecondOperand) {
                operator = nextOperator;
                return;
            }

            if (previousInput === null) {
                previousInput = inputValue;
            } else if (operator) {
                const result = performCalculation[operator](previousInput, inputValue);
                // Handle potential infinity or NaN from division by zero gracefully
                if (!isFinite(result)) {
                    currentInput = "Error";
                    previousInput = null;
                    operator = null;
                    waitingForSecondOperand = false;
                    return;
                }
                currentInput = String(result);
                previousInput = result;
            }

            waitingForSecondOperand = true;
            operator = nextOperator;
            updateDisplay();
        }

        const performCalculation = {
            '/': (firstOperand, secondOperand) => firstOperand / secondOperand,
            '*': (firstOperand, secondOperand) => firstOperand * secondOperand,
            '+': (firstOperand, secondOperand) => firstOperand + secondOperand,
            '-': (firstOperand, secondOperand) => firstOperand - secondOperand,
            '%': (firstOperand, secondOperand) => firstOperand % secondOperand
        };

        document.querySelectorAll('#calculator .calc-btn').forEach(button => {
            button.addEventListener('click', (event) => {
                const action = event.target.getAttribute('data-action');
                const value = event.target.getAttribute('data-value');

                if (action === 'number') {
                    inputNumber(value);
                } else if (action === 'decimal') {
                    inputDecimal();
                } else if (action === 'operator') {
                    handleOperator(value);
                } else if (action === 'calculate') {
                    handleOperator(operator); // Trigger calculation with the current operator
                    operator = null; // Reset operator after calculation
                } else if (action === 'clear') {
                    clear();
                    updateDisplay();
                }
            });
        });


        // --- BMI Logic (Same as before) ---
        document.getElementById('calculate-bmi').addEventListener('click', function() {
            const weight = parseFloat(document.getElementById('weight').value);
            const height = parseFloat(document.getElementById('height').value);
            const resultDiv = document.getElementById('bmi-result');
            const errorDiv = document.getElementById('bmi-error');

            resultDiv.classList.add('hidden');
            errorDiv.classList.add('hidden');

            if (isNaN(weight) || isNaN(height) || weight <= 0 || height <= 0) {
                errorDiv.classList.remove('hidden');
                return;
            }

            const bmi = weight / (height * height);
            const bmiValue = bmi.toFixed(2);
            let status = '';

            if (bmi < 18.5) {
                status = 'Underweight';
            } else if (bmi >= 18.5 && bmi < 24.9) {
                status = 'Healthy Weight';
            } else if (bmi >= 25 && bmi < 29.9) {
                status = 'Overweight';
            } else {
                status = 'Obese';
            }

            document.getElementById('bmi-value').textContent = bmiValue;
            document.getElementById('bmi-status').textContent = status;
            resultDiv.classList.remove('hidden');
        });


        // --- Currency Converter Logic (PKR and BHD rates updated) ---
        document.getElementById('convert-currency').addEventListener('click', function() {
            const amount = parseFloat(document.getElementById('amount').value);
            const fromCurrency = document.getElementById('from-currency').value;
            const toCurrency = document.getElementById('to-currency').value;
            const resultDiv = document.getElementById('conversion-result');
            const convertedValueSpan = document.getElementById('converted-value');

            resultDiv.classList.add('hidden');

            if (isNaN(amount) || amount < 0) {
                convertedValueSpan.textContent = 'Invalid Amount';
                resultDiv.classList.remove('hidden');
                return;
            }

            // Static sample exchange rates (USD as base for simplicity)
            // PKR and BHD added here
            const rates = {
                'USD': 1.00,
                'EUR': 0.92,
                'INR': 83.50,
                'GBP': 0.80,
                'JPY': 155.00,
                'PKR': 278.00, // Pakistani Rupee (Sample Rate)
                'BHD': 0.376  // Bahraini Dinar (Sample Rate - Pegged to USD)
            };

            if (fromCurrency === toCurrency) {
                 convertedValueSpan.textContent = `${amount.toFixed(2)} ${toCurrency}`;
            } else {
                // Convert from 'From Currency' to USD first, then to 'To Currency'
                const amountInUSD = amount / rates[fromCurrency];
                const convertedAmount = amountInUSD * rates[toCurrency];
                convertedValueSpan.textContent = `${convertedAmount.toFixed(2)} ${toCurrency}`;
            }
            
            resultDiv.classList.remove('hidden');
        });
    </script>
</body>
</html>
