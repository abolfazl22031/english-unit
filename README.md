# english-unit

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>English Unit - Modern Communication</title>
    <meta name="description" content="Interactive English learning unit for B2 level students">
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">
    <!-- Include EmailJS SDK -->
    <script src="https://cdn.jsdelivr.net/npm/@emailjs/browser@3/dist/email.min.js"></script>
    <script>
        // Initialize EmailJS with your public key
        (function(){
            emailjs.init("RNRIV7nBipH_Wnw8g"); // Public Key
        })();
    </script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: "#4F46E5",
                        secondary: "#10B981",
                        accent: "#F59E0B"
                    },
                    fontFamily: {
                        sans: ['"Open Sans"', 'sans-serif'],
                        display: ['"Poppins"', 'sans-serif']
                    }
                }
            }
        }
    </script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;600;700&family=Poppins:wght@500;600;700&display=swap');
        
        .section-content {
            display: none;
        }
        .section-content.active {
            display: block;
            animation: fadeIn 0.5s ease-in-out;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .audio-player {
            background-color: #f3f4f6;
            border-radius: 0.5rem;
            padding: 1rem;
        }
        .activity-box {
            border-left: 4px solid #4F46E5;
        }
   </style>
</head>
<body class="font-sans bg-gray-50 text-gray-800">
    <div class="container mx-auto px-4 py-8 max-w-6xl">
        <header class="text-center mb-12">
            <h1 class="text-4xl font-display font-bold text-primary mb-4">Modern Communication</h1>
            <p class="text-xl text-gray-600 mb-2">Unit 1 - Technology in Everyday Life</p>
            <p class="text-sm text-gray-500 mb-2">By Abolfazl Abdollahi and Andia Vahed</p>
            <p class="text-sm text-gray-500">Professor: Dr. Alikhani</p>
        </header>

        <div class="bg-white rounded-xl shadow-lg overflow-hidden mb-8">
            <div class="p-6 bg-gradient-to-r from-primary to-secondary">
                <h2 class="text-2xl font-display font-bold text-white">Unit Sections</h2>
            </div>
            <div class="grid grid-cols-2 md:grid-cols-4 gap-4 p-6">
                <button onclick="showSection('get-ready')" class="section-btn bg-accent hover:bg-yellow-600 text-white font-medium py-3 px-4 rounded-lg transition-all">
                    Get Ready
                </button>
                <button onclick="showSection('conversation')" class="section-btn bg-primary hover:bg-indigo-700 text-white font-medium py-3 px-4 rounded-lg transition-all">
                    Conversation
                </button>
                <button onclick="showSection('vocabulary')" class="section-btn bg-secondary hover:bg-emerald-600 text-white font-medium py-3 px-4 rounded-lg transition-all">
                    New Words
                </button>
                <button onclick="showSection('reading')" class="section-btn bg-purple-600 hover:bg-purple-700 text-white font-medium py-3 px-4 rounded-lg transition-all">
                    Reading
                </button>
                <button onclick="showSection('grammar')" class="section-btn bg-pink-600 hover:bg-pink-700 text-white font-medium py-3 px-4 rounded-lg transition-all">
                    Grammar
                </button>
                <button onclick="showSection('listening')" class="section-btn bg-blue-600 hover:bg-blue-700 text-white font-medium py-3 px-4 rounded-lg transition-all">
                    Listening
                </button>
                <button onclick="showSection('speaking')" class="section-btn bg-green-600 hover:bg-green-700 text-white font-medium py-3 px-4 rounded-lg transition-all">
                    Speaking
                </button>
                <button onclick="showSection('pronunciation')" class="section-btn bg-red-600 hover:bg-red-700 text-white font-medium py-3 px-4 rounded-lg transition-all">
                    Pronunciation
                </button>
                <button onclick="showSection('writing')" class="section-btn bg-teal-600 hover:bg-teal-700 text-white font-medium py-3 px-4 rounded-lg transition-all">
                    Writing
                </button>
                <button onclick="showSection('review')" class="section-btn bg-gray-600 hover:bg-gray-700 text-white font-medium py-3 px-4 rounded-lg transition-all">
                    What You Learned
                </button>
            </div>
        </div>

<!-- Get Ready Section -->
<div id="get-ready" class="section-content bg-white rounded-xl shadow-lg p-6 mb-8">
    <h2 class="text-2xl font-display font-bold text-primary mb-6 border-b pb-2">Get Ready</h2>
    <div class="mb-8">
        <img src="https://images.pexels.com/photos/3184296/pexels-photo-3184296.jpeg" alt="Modern communication with smartphones and laptops" class="w-full rounded-lg mb-6" loading="lazy">
        <p class="text-lg mb-6">Look at the pictures below. Match each phrase with the correct picture about technology use.</p>
    </div>
    <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-8">
        <div class="bg-gray-50 p-4 rounded-lg">
            <img src="https://images.pexels.com/photos/607812/pexels-photo-607812.jpeg" alt="Person checking Telegram on smartphone" class="w-full rounded mb-4" loading="lazy">
            <select class="w-full p-2 border rounded" id="get-ready-select1">
                <option value="" selected>Select a phrase</option>
                <option value="1">Checking Telegram</option>
                <option value="2">Online shopping</option>
                <option value="3">Video calling</option>
                <option value="4">Playing mobile games</option>
            </select>
        </div>
        <div class="bg-gray-50 p-4 rounded-lg">
            <img src="https://images.pexels.com/photos/265087/pexels-photo-265087.jpeg" alt="Person shopping online on laptop" class="w-full rounded mb-4" loading="lazy">
            <select class="w-full p-2 border rounded" id="get-ready-select2">
                <option value="" selected>Select a phrase</option>
                <option value="1">Checking Telegram</option>
                <option value="2">Online shopping</option>
                <option value="3">Video calling</option>
                <option value="4">Playing mobile games</option>
            </select>
        </div>
        <div class="bg-gray-50 p-4 rounded-lg">
            <img src="https://images.pexels.com/photos/7862598/pexels-photo-7862598.jpeg" alt="Person playing video game on smartphone" class="w-full rounded mb-4" loading="lazy">
            <select class="w-full p-2 border rounded" id="get-ready-select3">
                <option value="" selected>Select a phrase</option>
                <option value="1">Checking Telegram</option>
                <option value="2">Online shopping</option>
                <option value="3">Video calling</option>
                <option value="4">Playing mobile games</option>
            </select>
        </div>
        <div class="bg-gray-50 p-4 rounded-lg">
            <img src="https://images.pexels.com/photos/6325984/pexels-photo-6325984.jpeg" alt="Video calling on laptop" class="w-full rounded mb-4" loading="lazy">
            <select class="w-full p-2 border rounded" id="get-ready-select4">
                <option value="" selected>Select a phrase</option>
                <option value="1">Checking Telegram</option>
                <option value="2">Online shopping</option>
                <option value="3">Video calling</option>
                <option value="4">Playing mobile games</option>
            </select>
        </div>
    </div>
    <div class="activity-box bg-gray-50 p-6 rounded-lg mb-6">
        <h3 class="text-xl font-semibold mb-4">Activity 2: Discussion</h3>
        <p class="mb-4">Discuss these questions with a partner:</p>
        <ol class="list-decimal pl-6 space-y-3">
            <li>Which of these activities do you do most often?</li>
            <li>How has technology changed the way we communicate?</li>
            <li>What are some advantages and disadvantages of using technology for communication?</li>
        </ol>
        <div class="mt-4 p-4 bg-white rounded">
            <p class="text-gray-600 mb-2">Write your answers here:</p>
            <textarea class="w-full p-3 border rounded" rows="4" id="get-ready-textarea"></textarea>
        </div>
    </div>
    <div class="text-center mt-6">
        <input type="text" id="get-ready-name" class="w-full p-2 border rounded mb-4" placeholder="Enter your name (once per section)">
        <button onclick="submitSection('get-ready')" class="bg-primary hover:bg-indigo-700 text-white font-medium py-2 px-6 rounded-lg transition-all">
            Submit
        </button>
    </div>
</div>

<!-- Conversation Section -->
<div id="conversation" class="section-content bg-white rounded-xl shadow-lg p-6 mb-8">
    <h2 class="text-2xl font-display font-bold text-primary mb-6 border-b pb-2">Conversation</h2>
    <div class="mb-8">
        <img src="https://images.pexels.com/photos/3184297/pexels-photo-3184297.jpeg" alt="Sarah and Tom discussing technology use" class="w-full rounded-lg mb-6" loading="lazy">
        
        <div class="audio-player mb-8">
            <h3 class="text-lg font-semibold mb-2">Listen to the conversation:</h3>
            <audio controls class="w-full">
                <source src="https://media.vocaroo.com/mp3/18oC2m4pBkXz" type="audio/mpeg">
                Your browser does not support the audio element.
            </audio>
        </div>
        
        <div class="bg-blue-50 p-6 rounded-lg mb-6">
            <h3 class="text-xl font-semibold mb-4">Sarah and Tom discuss technology use:</h3>
            <div class="space-y-4">
                <p><strong>Sarah:</strong> "Tom, have you noticed how much time we spend on our phones these days?"</p>
                <p><strong>Tom:</strong> "Absolutely! I was just checking my screen time report, and it's about 4 hours daily. That's shocking!"</p>
                <p><strong>Sarah:</strong> "Mine's even higher. I think social media is the biggest time consumer for me."</p>
                <p><strong>Tom:</strong> "Same here. But I've started using app limiters to control my usage. Have you tried those?"</p>
                <p><strong>Sarah:</strong> "No, but I should. Do they really work?"</p>
                <p><strong>Tom:</strong> "They help, but you need willpower too. The best feature is the bedtime mode that turns the screen grayscale."</p>
                <p><strong>Sarah:</strong> "That's interesting! Maybe we should have a no-phone day together to experience life without screens."</p>
                <p><strong>Tom:</strong> "That's a great idea! How about this Saturday?"</p>
            </div>
        </div>
        
        <div class="activity-box bg-gray-50 p-6 rounded-lg mb-6">
            <h3 class="text-xl font-semibold mb-4">Activity 1: Comprehension</h3>
            <p class="mb-4">Answer these questions about the conversation:</p>
            <ol class="list-decimal pl-6 space-y-3 mb-4">
                <li>What is Tom's daily screen time?</li>
                <li>What does Sarah identify as her biggest time consumer?</li>
                <li>What solution has Tom tried to reduce phone usage?</li>
                <li>What do they plan to do together?</li>
            </ol>
            <div class="mt-4 p-4 bg-white rounded">
                <p class="text-gray-600 mb-2">Write your answers here:</p>
                <textarea class="w-full p-3 border rounded" rows="4" id="conversation-textarea1"></textarea>
            </div>
        </div>
        
        <div class="activity-box bg-gray-50 p-6 rounded-lg">
            <h3 class="text-xl font-semibold mb-4">Activity 2: Role Play</h3>
            <p class="mb-4">Practice the conversation with a partner, then create your own dialogue about technology use. Record your conversation and upload it.</p>
            <div class="mt-4 p-4 bg-white rounded">
                <p class="text-gray-600 mb-2">Upload your recording:</p>
                <input type="file" class="w-full p-2 border rounded" id="conversation-file">
            </div>
        </div>
    </div>
    <div class="text-center mt-6">
        <input type="text" id="conversation-name" class="w-full p-2 border rounded mb-4" placeholder="Enter your name (once per section)">
        <button onclick="submitSection('conversation')" class="bg-primary hover:bg-indigo-700 text-white font-medium py-2 px-6 rounded-lg transition-all">
            Submit
        </button>
    </div>
</div>

<!-- New Words Section -->
<div id="vocabulary" class="section-content bg-white rounded-xl shadow-lg p-6 mb-8">
    <h2 class="text-2xl font-display font-bold text-primary mb-6 border-b pb-2">New Words and Expressions</h2>
    <div class="mb-8">
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mb-8">
            <div class="bg-gray-50 p-4 rounded-lg">
                <h3 class="text-lg font-semibold mb-2">1. Digital native</h3>
                <p class="text-gray-700 mb-2">/ˈdɪdʒɪtəl ˈneɪtɪv/</p>
                <p class="italic">A person born or brought up during the age of digital technology.</p>
                <p class="mt-2"><strong>Example:</strong> "As digital natives, today's students are comfortable with technology."</p>
            </div>
            <div class="bg-gray-50 p-4 rounded-lg">
                <h3 class="text-lg font-semibold mb-2">2. Screen time</h3>
                <p class="text-gray-700 mb-2">/ˈskriːn taɪm/</p>
                <p class="italic">Time spent using a device with a screen such as a smartphone or computer.</p>
                <p class="mt-2"><strong>Example:</strong> "Parents should monitor their children's screen time."</p>
            </div>
            <div class="bg-gray-50 p-4 rounded-lg">
                <h3 class="text-lg font-semibold mb-2">3. App limiter</h3>
                <p class="text-gray-700 mb-2">/æp ˈlɪmɪtər/</p>
                <p class="italic">A tool that restricts the usage time of applications on devices.</p>
                <p class="mt-2"><strong>Example:</strong> "I set an app limiter for social media to 30 minutes per day."</p>
            </div>
            <div class="bg-gray-50 p-4 rounded-lg">
                <h3 class="text-lg font-semibold mb-2">4. Notification fatigue</h3>
                <p class="text-gray-700 mb-2">/ˌnoʊtɪfɪˈkeɪʃən fəˈtiːɡ/</p>
                <p class="italic">Feeling overwhelmed by too many alerts from apps and devices.</p>
                <p class="mt-2"><strong>Example:</strong> "She turned off notifications due to notification fatigue."</p>
            </div>
            <div class="bg-gray-50 p-4 rounded-lg">
                <h3 class="text-lg font-semibold mb-2">5. Phubbing</h3>
                <p class="text-gray-700 mb-2">/ˈfʌbɪŋ/</p>
                <p class="italic">The act of ignoring someone in favor of a mobile phone.</p>
                <p class="mt-2"><strong>Example:</strong> "Phubbing during dinner is considered rude."</p>
            </div>
            <div class="bg-gray-50 p-4 rounded-lg">
                <h3 class="text-lg font-semibold mb-2">6. Digital detox</h3>
                <p class="text-gray-700 mb-2">/ˈdɪdʒɪtəl ˈdiːtɒks/</p>
                <p class="italic">A period of time when a person refrains from using electronic devices.</p>
                <p class="mt-2"><strong>Example:</strong> "After his digital detox, he felt more focused and relaxed."</p>
            </div>
        </div>
        
        <div class="activity-box bg-gray-50 p-6 rounded-lg mb-6">
            <h3 class="text-xl font-semibold mb-4">Activity 1: Matching</h3>
            <p class="mb-4">Match each word with its correct definition:</p>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-4">
                <div class="bg-white p-3 rounded border">
                    <p class="font-medium">1. Digital native</p>
                    <select class="w-full mt-2 p-2 border rounded" id="vocabulary-select1">
                        <option value="">Select definition</option>
                        <option value="a">A tool that restricts app usage time</option>
                        <option value="b">A person comfortable with digital technology</option>
                        <option value="c">Ignoring someone for your phone</option>
                    </select>
                </div>
                <div class="bg-white p-3 rounded border">
                    <p class="font-medium">2. Phubbing</p>
                    <select class="w-full mt-2 p-2 border rounded" id="vocabulary-select2">
                        <option value="">Select definition</option>
                        <option value="a">A tool that restricts app usage time</option>
                        <option value="b">A person comfortable with digital technology</option>
                        <option value="c">Ignoring someone for your phone</option>
                    </select>
                </div>
            </div>
        </div>
        
        <div class="activity-box bg-gray-50 p-6 rounded-lg">
            <h3 class="text-xl font-semibold mb-4">Activity 2: Sentence Completion</h3>
            <p class="mb-4">Complete these sentences with the new vocabulary words:</p>
            <div class="space-y-4">
                <div class="bg-white p-3 rounded border">
                    <p>After experiencing __________, Mark decided to turn off all non-essential alerts on his phone.</p>
                    <input type="text" class="w-full mt-2 p-2 border rounded" id="vocabulary-input1" placeholder="Type the word">
                </div>
                <div class="bg-white p-3 rounded border">
                    <p>Many __________ find it hard to imagine life without smartphones and the internet.</p>
                    <input type="text" class="w-full mt-2 p-2 border rounded" id="vocabulary-input2" placeholder="Type the word">
                </div>
            </div>
        </div>
    </div>
    <div class="text-center mt-6">
        <input type="text" id="vocabulary-name" class="w-full p-2 border rounded mb-4" placeholder="Enter your name (once per section)">
        <button onclick="submitSection('vocabulary')" class="bg-primary hover:bg-indigo-700 text-white font-medium py-2 px-6 rounded-lg transition-all">
            Submit
        </button>
    </div>
</div>

<!-- Reading Section -->
<div id="reading" class="section-content bg-white rounded-xl shadow-lg p-6 mb-8">
    <h2 class="text-2xl font-display font-bold text-primary mb-6 border-b pb-2">Reading</h2>
    <div class="mb-8">
        <div class="bg-gray-50 p-6 rounded-lg mb-6">
            <h3 class="text-xl font-semibold mb-4">Smartphones and Communication</h3>
            <img src="https://images.pexels.com/photos/267350/pexels-photo-267350.jpeg" alt="People using smartphones for communication" class="w-full rounded-lg mb-6" loading="lazy">
            
            <div class="space-y-4 text-lg leading-relaxed">
                <p>Smartphones are very important for digital natives. People have been using smartphones for many years to talk, send messages, and use social media. They help us stay connected, but too much screen time can cause problems.</p>
                
                <p>For example, phubbing is when you ignore someone because you are looking at your phone. This can make people feel sad or unimportant. Also, many people have been feeling notification fatigue because they get too many alerts from apps.</p>
                
                <p>To solve these problems, some people try a digital detox. This means they stop using their phones for a short time. Others use app limiters to control how much time they spend on apps. Balancing phone use is important for good communication.</p>
            </div>
        </div>
        
        <div class="activity-box bg-gray-50 p-6 rounded-lg mb-6">
            <h3 class="text-xl font-semibold mb-4">Activity 1: True/False</h3>
            <p class="mb-4">Mark these statements as True (T) or False (F) according to the text:</p>
            <div class="space-y-3">
                <div class="flex items-center">
                    <input type="radio" name="q1" id="q1-t" class="mr-2" value="T">
                    <label for="q1-t" class="mr-4">T</label>
                    <input type="radio" name="q1" id="q1-f" class="mr-2" value="F">
                    <label for="q1-f">F</label>
                    <span class="ml-4">1. Phubbing means ignoring someone to use your phone.</span>
                </div>
                <div class="flex items-center">
                    <input type="radio" name="q2" id="q2-t" class="mr-2" value="T">
                    <label for="q2-t" class="mr-4">T</label>
                    <input type="radio" name="q2" id="q2-f" class="mr-2" value="F">
                    <label for="q2-f">F</label>
                    <span class="ml-4">2. A digital detox means using your phone more.</span>
                </div>
                <div class="flex items-center">
                    <input type="radio" name="q3" id="q3-t" class="mr-2" value="T">
                    <label for="q3-t" class="mr-4">T</label>
                    <input type="radio" name="q3" id="q3-f" class="mr-2" value="F">
                    <label for="q3-f">F</label>
                    <span class="ml-4">3. App limiters help control screen time.</span>
                </div>
            </div>
        </div>
        
        <div class="activity-box bg-gray-50 p-6 rounded-lg mb-6">
            <h3 class="text-xl font-semibold mb-4">Activity 2: Comprehension Questions</h3>
            <p class="mb-4">Answer these questions according to the text:</p>
            <div class="space-y-4">
                <div>
                    <p class="font-medium">1. Why do some people feel notification fatigue?</p>
                    <textarea class="w-full mt-2 p-3 border rounded" rows="2" id="reading-textarea1" placeholder="Your answer"></textarea>
                </div>
                <div>
                    <p class="font-medium">2. What is one way to manage screen time mentioned in the text?</p>
                    <textarea class="w-full mt-2 p-3 border rounded" rows="2" id="reading-textarea2" placeholder="Your answer"></textarea>
                </div>
            </div>
        </div>
        
        <div class="activity-box bg-gray-50 p-6 rounded-lg">
            <h3 class="text-xl font-semibold mb-4">Activity 3: Vocabulary in Context</h3>
            <p class="mb-4">Find words in the text that match these definitions:</p>
            <div class="space-y-4">
                <div class="bg-white p-3 rounded border">
                    <p>1. Ignoring someone to look at your phone (paragraph 2)</p>
                    <input type="text" class="w-full mt-2 p-2 border rounded" id="reading-input1" placeholder="Type the word">
                </div>
                <div class="bg-white p-3 rounded border">
                    <p>2. A break from using electronic devices (paragraph 3)</p>
                    <input type="text" class="w-full mt-2 p-2 border rounded" id="reading-input2" placeholder="Type the word">
                </div>
            </div>
        </div>
    </div>
    <div class="text-center mt-6">
        <input type="text" id="reading-name" class="w-full p-2 border rounded mb-4" placeholder="Enter your name (once per section)">
        <button onclick="submitSection('reading')" class="bg-primary hover:bg-indigo-700 text-white font-medium py-2 px-6 rounded-lg transition-all">
            Submit
        </button>
    </div>
</div>

<!-- Grammar Section -->
<div id="grammar" class="section-content bg-white rounded-xl shadow-lg p-6 mb-8">
    <h2 class="text-2xl font-display font-bold text-primary mb-6 border-b pb-2">Grammar</h2>
    <div class="mb-8">
        <div class="bg-gray-50 p-6 rounded-lg mb-6">
            <h3 class="text-xl font-semibold mb-4">Present Perfect Continuous</h3>
            <p class="mb-4 text-lg">We use the present perfect continuous to talk about:</p>
            <ul class="list-disc pl-6 space-y-2 mb-6">
                <li>Actions that started in the past and are still continuing</li>
                <li>Actions that have recently stopped but have present results</li>
            </ul>
            
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-6">
                <div class="bg-white p-4 rounded border">
                    <h4 class="font-semibold mb-2">Form:</h4>
                    <p>Subject + have/has + been + verb-ing</p>
                    <p class="mt-2 italic">"I have been studying English for three years."</p>
                </div>
                <div class="bg-white p-4 rounded border">
                    <h4 class="font-semibold mb-2">Common time expressions:</h4>
                    <p>for, since, all day/week, lately, recently</p>
                    <p class="mt-2 italic">"She has been working here since 2015."</p>
                </div>
            </div>
            
            <h4 class="font-semibold mb-2">Examples from our topic:</h4>
            <div class="space-y-3 italic pl-4 border-l-4 border-primary">
                <p>"People have been using smartphones more frequently in recent years."</p>
                <p>"He has been experiencing notification fatigue lately."</p>
                <p>"How long have you been limiting your screen time?"</p>
            </div>
        </div>
        
        <div class="activity-box bg-gray-50 p-6 rounded-lg mb-6">
            <h3 class="text-xl font-semibold mb-4">Activity 1: Sentence Formation</h3>
            <p class="mb-4">Complete these sentences using the present perfect continuous:</p>
            <div class="space-y-4">
                <div class="bg-white p-3 rounded border">
                    <p>1. I __________ (study) English __________ five years.</p>
                    <div class="grid grid-cols-2 gap-2 mt-2">
                        <input type="text" class="p-2 border rounded" id="grammar-input1-1" placeholder="verb form">
                        <input type="text" class="p-2 border rounded" id="grammar-input1-2" placeholder="time expression">
                    </div>
                </div>
                <div class="bg-white p-3 rounded border">
                    <p>2. She __________ (use) app limiters __________ last month.</p>
                    <div class="grid grid-cols-2 gap-2 mt-2">
                        <input type="text" class="p-2 border rounded" id="grammar-input2-1" placeholder="verb form">
                        <input type="text" class="p-2 border rounded" id="grammar-input2-2" placeholder="time expression">
                    </div>
                </div>
            </div>
        </div>
        
        <div class="activity-box bg-gray-50 p-6 rounded-lg">
            <h3 class="text-xl font-semibold mb-4">Activity 2: Error Correction</h3>
            <p class="mb-4">Correct the mistakes in these sentences:</p>
            <div class="space-y-4">
                <div class="bg-white p-3 rounded border">
                    <p>1. They have use smartphones for many years.</p>
                    <input type="text" class="w-full mt-2 p-2 border rounded" id="grammar-input3" placeholder="Corrected sentence">
                </div>
                <div class="bg-white p-3 rounded border">
                    <p>2. We has been discussing digital detox lately.</p>
                    <input type="text" class="w-full mt-2 p-2 border rounded" id="grammar-input4" placeholder="Corrected sentence">
                </div>
            </div>
        </div>
    </div>
    <div class="text-center mt-6">
        <input type="text" id="grammar-name" class="w-full p-2 border rounded mb-4" placeholder="Enter your name (once per section)">
        <button onclick="submitSection('grammar')" class="bg-primary hover:bg-indigo-700 text-white font-medium py-2 px-6 rounded-lg transition-all">
            Submit
        </button>
    </div>
</div>

<!-- Listening Section -->
<div id="listening" class="section-content bg-white rounded-xl shadow-lg p-6 mb-8">
    <h2 class="text-2xl font-display font-bold text-primary mb-6 border-b pb-2">Listening</h2>
    <div class="audio-player mb-8">
        <h3 class="text-lg font-semibold mb-2">Listen to the audio about digital wellbeing:</h3>
        <iframe src="https://voca.ro/1hUYCSIRpVTf" width="100%" height="100" frameborder="0" allow="autoplay"></iframe>
    </div>

                
                <div class="activity-box bg-gray-50 p-6 rounded-lg mb-6">
                    <h3 class="text-xl font-semibold mb-4">Activity 1: Identification</h3>
                    <p class="mb-4">Listen and identify which words you hear from our vocabulary list:</p>
                    <div class="grid grid-cols-2 md:grid-cols-3 gap-4">
                        <div class="flex items-center">
                            <input type="checkbox" id="word1" class="mr-2" value="Digital native">
                            <label for="word1">Digital native</label>
                        </div>
                        <div class="flex items-center">
                            <input type="checkbox" id="word2" class="mr-2" value="Screen time">
                            <label for="word2">Screen time</label>
                        </div>
                        <div class="flex items-center">
                            <input type="checkbox" id="word3" class="mr-2" value="Notification fatigue">
                            <label for="word3">Notification fatigue</label>
                        </div>
                        <div class="flex items-center">
                            <input type="checkbox" id="word4" class="mr-2" value="Phubbing">
                            <label for="word4">Phubbing</label>
                        </div>
                        <div class="flex items-center">
                            <input type="checkbox" id="word5" class="mr-2" value="Digital detox">
                            <label for="word5">Digital detox</label>
                        </div>
                        <div class="flex items-center">
                            <input type="checkbox" id="word6" class="mr-2" value="App limiter">
                            <label for="word6">App limiter</label>
                        </div>
                    </div>
                </div>
                
                <div class="activity-box bg-gray-50 p-6 rounded-lg mb-6">
                    <h3 class="text-xl font-semibold mb-4">Activity 2: Main Ideas</h3>
                    <p class="mb-4">What are the three main suggestions mentioned in the audio for improving digital wellbeing?</p>
                    <div class="space-y-3">
                        <div class="bg-white p-3 rounded border">
                            <input type="text" class="w-full p-2 border rounded" id="listening-input1" placeholder="First suggestion">
                        </div>
                        <div class="bg-white p-3 rounded border">
                            <input type="text" class="w-full p-2 border rounded" id="listening-input2" placeholder="Second suggestion">
                        </div>
                        <div class="bg-white p-3 rounded border">
                            <input type="text" class="w-full p-2 border rounded" id="listening-input3" placeholder="Third suggestion">
                        </div>
                    </div>
                </div>
                
                <div class="activity-box bg-gray-50 p-6 rounded-lg">
                    <h3 class="text-xl font-semibold mb-4">Activity 3: Detail Orientation</h3>
                    <p class="mb-4">Listen again and answer these specific questions:</p>
                    <div class="space-y-4">
                        <div>
                            <p class="font-medium">1. What percentage of people check their phones within 15 minutes of waking up?</p>
                            <input type="text" class="w-full mt-2 p-2 border rounded" id="listening-input4" placeholder="Your answer">
                        </div>
                        <div>
                            <p class="font-medium">2. How many hours of screen time per day does the speaker recommend as a maximum?</p>
                            <input type="text" class="w-full mt-2 p-2 border rounded" id="listening-input5" placeholder="Your answer">
                        </div>
                    </div>
                </div>
            </div>
    <div class="text-center mt-6">
        <input type="text" id="listening-name" class="w-full p-2 border rounded mb-4" placeholder="Enter your name (once per section)">
        <button onclick="submitSection('listening')" class="bg-primary hover:bg-indigo-700 text-white font-medium py-2 px-6 rounded-lg transition-all">
            Submit
        </button>
    </div>
</div>

<!-- Speaking Section -->
<div id="speaking" class="section-content bg-white rounded-xl shadow-lg p-6 mb-8">
    <h2 class="text-2xl font-display font-bold text-primary mb-6 border-b pb-2">Speaking</h2>
    <div class="mb-8">
        <div class="bg-gray-50 p-6 rounded-lg mb-6">
            <h3 class="text-xl font-semibold mb-4">Discussion Topics</h3>
            <p class="mb-4">Prepare to discuss these questions with a partner. Record your discussion and upload it.</p>
            
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-6">
                <div class="bg-white p-4 rounded-lg border">
                    <h4 class="font-semibold mb-2">Topic 1: Personal Habits</h4>
                    <ul class="list-disc pl-5 space-y-1">
                        <li>How much screen time do you have daily?</li>
                        <li>Which apps do you use most frequently?</li>
                        <li>Have you tried to reduce your phone usage? How?</li>
                    </ul>
                </div>
                <div class="bg-white p-4 rounded-lg border">
                    <h4 class="font-semibold mb-2">Topic 2: Social Impact</h4>
                    <ul class="list-disc pl-5 space-y-1">
                        <li>How has technology changed communication?</li>
                        <li>What are the positive and negative effects?</li>
                        <li>Do you think phubbing is a serious problem? Why?</li>
                    </ul>
                </div>
            </div>
            
            <div class="bg-white p-4 rounded-lg border">
                <h4 class="font-semibold mb-2">Useful Expressions:</h4>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                    <div>
                        <p class="font-medium">Giving Opinions:</p>
                        <ul class="list-disc pl-5">
                            <li>"In my view..."</li>
                            <li>"I strongly believe that..."</li>
                            <li>"From my perspective..."</li>
                        </ul>
                    </div>
                    <div>
                        <p class="font-medium">Agreeing/Disagreeing:</p>
                        <ul class="list-disc pl-5">
                            <li>"I see your point, but..."</li>
                            <li>"That's a valid point, however..."</li>
                            <li>"I completely agree because..."</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="activity-box bg-gray-50 p-6 rounded-lg">
            <h3 class="text-xl font-semibold mb-4">Activity: Recorded Discussion</h3>
            <p class="mb-4">Record your discussion (3-5 minutes) about one of the topics above. Focus on:</p>
            <ul class="list-disc pl-6 mb-4 space-y-1">
                <li>Using the present perfect continuous tense</li>
                <li>Incorporating our new vocabulary words</li>
                <li>Speaking clearly and expressing your ideas fully</li>
            </ul>
            <div class="mt-4 p-4 bg-white rounded">
                <p class="text-gray-600 mb-2">Upload your recording:</p>
                <input type="file" class="w-full p-2 border rounded" id="speaking-file">
            </div>
        </div>
    </div>
    <div class="text-center mt-6">
        <input type="text" id="speaking-name" class="w-full p-2 border rounded mb-4" placeholder="Enter your name (once per section)">
        <button onclick="submitSection('speaking')" class="bg-primary hover:bg-indigo-700 text-white font-medium py-2 px-6 rounded-lg transition-all">
            Submit
        </button>
    </div>
</div>

<!-- Pronunciation Section -->
<div id="pronunciation" class="section-content bg-white rounded-xl shadow-lg p-6 mb-8">
    <h2 class="text-2xl font-display font-bold text-primary mb-6 border-b pb-2">Pronunciation</h2>
    <div class="mb-8">
        <div class="bg-gray-50 p-6 rounded-lg mb-6">
            <h3 class="text-xl font-semibold mb-4">Word Stress in Compound Nouns</h3>
            <p class="mb-4">In English, compound nouns (two words that function as one) usually have stress on the first word:</p>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-4 mb-6">
                <div class="bg-white p-4 rounded text-center">
                    <p class="text-lg font-medium">ˈscreen time</p>
                    <p class="text-gray-600">(not screen ˈtime)</p>
                </div>
                <div class="bg-white p-4 rounded text-center">
                    <p class="text-lg font-medium">ˈsmartphone</p>
                    <p class="text-gray-600">(not smart ˈphone)</p>
                </div>
                <div class="bg-white p-4 rounded text-center">
                    <p class="text-lg font-medium">ˈapp limiter</p>
                    <p class="text-gray-600">(not app ˈlimiter)</p>
                </div>
            </div>
            
           <div class="audio-player mb-6">
    <h4 class="text-lg font-semibold mb-2">Listen and repeat:</h4>
    <iframe src="https://voca.ro/13p9rSG8G5hM" width="100%" height="100" frameborder="0" allow="autoplay"></iframe>
</div>

            
            <h4 class="text-lg font-semibold mb-2">Practice these compound nouns from our unit:</h4>
            <div class="grid grid-cols-2 md:grid-cols-4 gap-4">
                <div class="bg-white p-3 rounded border text-center">
                    <p>digital native</p>
                </div>
                <div class="bg-white p-3 rounded border text-center">
                    <p>notification fatigue</p>
                </div>
                <div class="bg-white p-3 rounded border text-center">
                    <p>digital detox</p>
                </div>
                <div class="bg-white p-3 rounded border text-center">
                    <p>social media</p>
                </div>
            </div>
        </div>
        
        <div class="activity-box bg-gray-50 p-6 rounded-lg">
            <h3 class="text-xl font-semibold mb-4">Activity: Stress Identification</h3>
            <p class="mb-4">Listen to these words and mark where you hear the primary stress:</p>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                <div>
                    <p class="font-medium mb-2">1. smartphone</p>
                    <div class="flex space-x-4">
                        <div class="flex items-center">
                            <input type="radio" name="stress1" id="stress1-1" class="mr-2" value="SMARTphone">
                            <label for="stress1-1">SMARTphone</label>
                        </div>
                        <div class="flex items-center">
                            <input type="radio" name="stress1" id="stress1-2" class="mr-2" value="smartPHONE">
                            <label for="stress1-2">smartPHONE</label>
                        </div>
                    </div>
                </div>
                <div>
                    <p class="font-medium mb-2">2. screen time</p>
                    <div class="flex space-x-4">
                        <div class="flex items-center">
                            <input type="radio" name="stress2" id="stress2-1" class="mr-2" value="SCREENtime">
                            <label for="stress2-1">SCREENtime</label>
                        </div>
                        <div class="flex items-center">
                            <input type="radio" name="stress2" id="stress2-2" class="mr-2" value="screenTIME">
                            <label for="stress2-2">screenTIME</label>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div class="text-center mt-6">
        <input type="text" id="pronunciation-name" class="w-full p-2 border rounded mb-4" placeholder="Enter your name (once per section)">
        <button onclick="submitSection('pronunciation')" class="bg-primary hover:bg-indigo-700 text-white font-medium py-2 px-6 rounded-lg transition-all">
            Submit
        </button>
    </div>
</div>

<!-- Writing Section -->
<div id="writing" class="section-content bg-white rounded-xl shadow-lg p-6 mb-8">
    <h2 class="text-2xl font-display font-bold text-primary mb-6 border-b pb-2">Writing</h2>
    <div class="mb-8">
        <div class="bg-gray-50 p-6 rounded-lg mb-6">
            <h3 class="text-xl font-semibold mb-4">Opinion Essay: Smartphones and Communication</h3>
            <p class="mb-4">Write a 100–150 word essay expressing your opinion on this statement:</p>
            <blockquote class="bg-white p-4 border-l-4 border-primary italic mb-6">
                "Smartphones have helped communication more than they have harmed it."
            </blockquote>
            
            <h4 class="font-semibold mb-2">Structure your essay with:</h4>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-4 mb-6">
                <div class="bg-white p-3 rounded border">
                    <h5 class="font-medium mb-1">Introduction</h5>
                    <p class="text-sm">Say what you think</p>
                </div>
                <div class="bg-white p-3 rounded border">
                    <h5 class="font-medium mb-1">Body Paragraph</h5>
                    <p class="text-sm">Give 1–2 reasons to support your opinion</p>
                </div>
                <div class="bg-white p-3 rounded border">
                    <h5 class="font-medium mb-1">Conclusion</h5>
                    <p class="text-sm">Repeat your opinion shortly</p>
                </div>
            </div>
            
            <h4 class="font-semibold mb-2">Useful Vocabulary:</h4>
            <div class="flex flex-wrap gap-2 mb-4">
                <span class="bg-white px-3 py-1 rounded-full border text-sm">for example</span>
                <span class="bg-white px-3 py-1 rounded-full border text-sm">however</span>
                <span class="bg-white px-3 py-1 rounded-full border text-sm">in my opinion</span>
                <span class="bg-white px-3 py-1 rounded-full border text-sm">digital native</span>
                <span class="bg-white px-3 py-1 rounded-full border text-sm">screen time</span>
                <span class="bg-white px-3 py-1 rounded-full border text-sm">phubbing</span>
                <span class="bg-white px-3 py-1 rounded-full border text-sm">digital detox</span>
            </div>
        </div>
        
        <div class="activity-box bg-gray-50 p-6 rounded-lg">
            <h3 class="text-xl font-semibold mb-4">Write Your Essay</h3>
            <textarea class="w-full p-4 border rounded min-h-[200px]" id="writing-textarea" placeholder="Type your essay here..."></textarea>
            <button class="mt-4 bg-primary hover:bg-indigo-700 text-white font-medium py-2 px-6 rounded-lg transition-all">
                Submit
            </button>
        </div>
    </div>
    <div class="text-center mt-6">
        <input type="text" id="writing-name" class="w-full p-2 border rounded mb-4" placeholder="Enter your name (once per section)">
        <button onclick="submitSection('writing')" class="bg-primary hover:bg-indigo-700 text-white font-medium py-2 px-6 rounded-lg transition-all">
            Submit
        </button>
    </div>
</div>

<!-- Review Section -->
<div id="review" class="section-content bg-white rounded-xl shadow-lg p-6 mb-8">
    <h2 class="text-2xl font-display font-bold text-primary mb-6 border-b pb-2">What You Learned</h2>
    <div class="mb-8">
        <div class="bg-gray-50 p-6 rounded-lg mb-6">
            <h3 class="text-xl font-semibold mb-4">Unit Summary</h3>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-6">
                <div>
                    <h4 class="font-semibold mb-2 text-secondary">Vocabulary</h4>
                    <ul class="list-disc pl-5 space-y-1">
                        <li>Digital native</li>
                        <li>Screen time</li>
                        <li>App limiter</li>
                        <li>Notification fatigue</li>
                        <li>Phubbing</li>
                        <li>Digital detox</li>
                    </ul>
                </div>
                <div>
                    <h4 class="font-semibold mb-2 text-secondary">Grammar</h4>
                    <ul class="list-disc pl-5 space-y-1">
                        <li>Present perfect continuous</li>
                        <li>Form: have/has + been + verb-ing</li>
                        <li>Usage: ongoing actions with present results</li>
                    </ul>
                </div>
                </div>
                
                <h4 class="font-semibold mb-2 text-secondary">Key Concepts</h4>
                <ul class="list-disc pl-5 space-y-2">
                    <li>Technology has changed communication patterns significantly</li>
                    <li>Excessive screen time can have negative social effects</li>
                    <li>There are strategies to manage technology use effectively</li>
                    <li>Balance is important in digital communication</li>
                </ul>
            </div>
            
            <div class="activity-box bg-gray-50 p-6 rounded-lg mb-6">
                <h3 class="text-xl font-semibold mb-4">Self-Evaluation</h3>
                <p class="mb-4">Rate your understanding of these unit components (1 = not confident, 5 = very confident):</p>
                <div class="space-y-4">
                    <div>
                        <p class="font-medium mb-1">Vocabulary from this unit</p>
                        <div class="flex space-x-2">
                            <button class="w-8 h-8 rounded-full border flex items-center justify-center" data-value="1">1</button>
                            <button class="w-8 h-8 rounded-full border flex items-center justify-center" data-value="2">2</button>
                            <button class="w-8 h-8 rounded-full border flex items-center justify-center" data-value="3">3</button>
                            <button class="w-8 h-8 rounded-full border flex items-center justify-center" data-value="4">4</button>
                            <button class="w-8 h-8 rounded-full border flex items-center justify-center" data-value="5">5</button>
                        </div>
                    </div>
                    <div>
                        <p class="font-medium mb-1">Present perfect continuous</p>
                        <div class="flex space-x-2">
                            <button class="w-8 h-8 rounded-full border flex items-center justify-center" data-value="1">1</button>
                            <button class="w-8 h-8 rounded-full border flex items-center justify-center" data-value="2">2</button>
                            <button class="w-8 h-8 rounded-full border flex items-center justify-center" data-value="3">3</button>
                            <button class="w-8 h-8 rounded-full border flex items-center justify-center" data-value="4">4</button>
                            <button class="w-8 h-8 rounded-full border flex items-center justify-center" data-value="5">5</button>
                        </div>
                    </div>
                    <div>
                        <p class="font-medium mb-1">Discussion about technology</p>
                        <div class="flex space-x-2">
                            <button class="w-8 h-8 rounded-full border flex items-center justify-center" data-value="1">1</button>
                            <button class="w-8 h-8 rounded-full border flex items-center justify-center" data-value="2">2</button>
                            <button class="w-8 h-8 rounded-full border flex items-center justify-center" data-value="3">3</button>
                            <button class="w-8 h-8 rounded-full border flex items-center justify-center" data-value="4">4</button>
                            <button class="w-8 h-8 rounded-full border flex items-center justify-center" data-value="5">5</button>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="activity-box bg-gray-50 p-6 rounded-lg">
                <h3 class="text-xl font-semibold mb-4">Reflection</h3>
                <p class="mb-4">Answer these questions to reflect on your learning:</p>
                <div class="space-y-4">
                    <div>
                        <p class="font-medium">What was the most useful thing you learned in this unit?</p>
                        <textarea class="w-full mt-2 p-3 border rounded" rows="2" id="review-textarea1" placeholder="Your answer"></textarea>
                    </div>
                    <div>
                        <p class="font-medium">What area do you need to practice more?</p>
                        <textarea class="w-full mt-2 p-3 border rounded" rows="2" id="review-textarea2" placeholder="Your answer"></textarea>
                    </div>
                    <div>
                        <p class="font-medium">How will you apply what you learned about technology use in your daily life?</p>
                        <textarea class="w-full mt-2 p-3 border rounded" rows="2" id="review-textarea3" placeholder="Your answer"></textarea>
                    </div>
                </div>
            </div>
        </div>
    <div class="text-center mt-6">
        <input type="text" id="review-name" class="w-full p-2 border rounded mb-4" placeholder="Enter your name (once per section)">
        <button onclick="submitSection('review')" class="bg-primary hover:bg-indigo-700 text-white font-medium py-2 px-6 rounded-lg transition-all">
            Submit
        </button>
    </div>
</div>

        <footer class="text-center py-8 text-gray-500">
            <p>© 2023 English Learning Unit | B2 Level</p>
        </footer>
    </div>

    <script>
        // Show the selected section and hide others
        function showSection(sectionId) {
            document.querySelectorAll('.section-content').forEach(section => {
                section.classList.remove('active');
            });
            document.getElementById(sectionId).classList.add('active');
            document.getElementById(sectionId).scrollIntoView({ behavior: 'smooth' });
        }
        
        document.addEventListener('DOMContentLoaded', function() {
            showSection('get-ready');
        });

        function submitSection(sectionId) {
            const nameInput = document.getElementById(`${sectionId}-name`).value;
            if (!nameInput) {
                alert('Please enter your name before submitting.');
                return;
            }

            let message = `Section: ${sectionId}\nName: ${nameInput}\n`;

            switch (sectionId) {
                case 'get-ready':
                    message += `Activity 1:\n- Select 1: ${document.getElementById('get-ready-select1').value}\n- Select 2: ${document.getElementById('get-ready-select2').value}\n- Select 3: ${document.getElementById('get-ready-select3').value}\n- Select 4: ${document.getElementById('get-ready-select4').value}\n`;
                    message += `Activity 2:\n${document.getElementById('get-ready-textarea').value}\n`;
                    break;
                case 'conversation':
                    message += `Activity 1:\n${document.getElementById('conversation-textarea1').value}\n`;
                    const conversationFile = document.getElementById('conversation-file').files[0];
                    if (conversationFile) {
                        message += `Activity 2: File attached (name: ${conversationFile.name})\n`;
                    }
                    break;
                case 'vocabulary':
                    message += `Activity 1:\n- Select 1: ${document.getElementById('vocabulary-select1').value}\n- Select 2: ${document.getElementById('vocabulary-select2').value}\n`;
                    message += `Activity 2:\n- Input 1: ${document.getElementById('vocabulary-input1').value}\n- Input 2: ${document.getElementById('vocabulary-input2').value}\n`;
                    break;
                case 'reading':
                    message += `Activity 1:\n- Q1: ${document.querySelector('input[name="q1"]:checked') ? document.querySelector('input[name="q1"]:checked').value : ''}\n- Q2: ${document.querySelector('input[name="q2"]:checked') ? document.querySelector('input[name="q2"]:checked').value : ''}\n- Q3: ${document.querySelector('input[name="q3"]:checked') ? document.querySelector('input[name="q3"]:checked').value : ''}\n`;
                    message += `Activity 2:\n- Q1: ${document.getElementById('reading-textarea1').value}\n- Q2: ${document.getElementById('reading-textarea2').value}\n`;
                    message += `Activity 3:\n- Input 1: ${document.getElementById('reading-input1').value}\n- Input 2: ${document.getElementById('reading-input2').value}\n`;
                    break;
                case 'grammar':
                    message += `Activity 1:\n- Sentence 1: ${document.getElementById('grammar-input1-1').value} ${document.getElementById('grammar-input1-2').value}\n- Sentence 2: ${document.getElementById('grammar-input2-1').value} ${document.getElementById('grammar-input2-2').value}\n`;
                    message += `Activity 2:\n- Sentence 1: ${document.getElementById('grammar-input3').value}\n- Sentence 2: ${document.getElementById('grammar-input4').value}\n`;
                    break;
                case 'listening':
                    const checkedWords = [];
                    document.querySelectorAll('#listening input[type="checkbox"]:checked').forEach(checkbox => {
                        checkedWords.push(checkbox.value);
                    });
                    message += `Activity 1:\n- Words: ${checkedWords.join(', ')}\n`;
                    message += `Activity 2:\n- Suggestion 1: ${document.getElementById('listening-input1').value}\n- Suggestion 2: ${document.getElementById('listening-input2').value}\n- Suggestion 3: ${document.getElementById('listening-input3').value}\n`;
                    message += `Activity 3:\n- Q1: ${document.getElementById('listening-input4').value}\n- Q2: ${document.getElementById('listening-input5').value}\n`;
                    break;
                case 'speaking':
                    const speakingFile = document.getElementById('speaking-file').files[0];
                    if (speakingFile) {
                        message += `Activity: File attached (name: ${speakingFile.name})\n`;
                    }
                    break;
                case 'pronunciation':
                    message += `Activity:\n- Stress 1: ${document.querySelector('input[name="stress1"]:checked') ? document.querySelector('input[name="stress1"]:checked').value : ''}\n- Stress 2: ${document.querySelector('input[name="stress2"]:checked') ? document.querySelector('input[name="stress2"]:checked').value : ''}\n`;
                    break;
                case 'writing':
                    message += `Essay:\n${document.getElementById('writing-textarea').value}\n`;
                    break;
                case 'review':
                    const vocabRating = document.querySelector('#review button[data-value]:focus') ? document.querySelector('#review button[data-value]:focus').getAttribute('data-value') : '';
                    const grammarRating = document.querySelectorAll('#review button[data-value]:focus')[1] ? document.querySelectorAll('#review button[data-value]:focus')[1].getAttribute('data-value') : '';
                    const discussionRating = document.querySelectorAll('#review button[data-value]:focus')[2] ? document.querySelectorAll('#review button[data-value]:focus')[2].getAttribute('data-value') : '';
                    message += `Self-Evaluation:\n- Vocabulary: ${vocabRating}\n- Grammar: ${grammarRating}\n- Discussion: ${discussionRating}\n`;
                    message += `Reflection:\n- Most Useful: ${document.getElementById('review-textarea1').value}\n- Need Practice: ${document.getElementById('review-textarea2').value}\n- Apply: ${document.getElementById('review-textarea3').value}\n`;
                    break;
            }

            // Send email using EmailJS
            const emailParams = {
                to_email: "abolfazlabdollahi199@gmail.com", // Destination email
                from_name: nameInput,
                message: message,
                service_id: "service_zcjng72", // Service ID
                template_id: "template_vuyocki" // Template ID
            };

            emailjs.send("service_zcjng72", "template_vuyocki", emailParams)
                .then(function(response) {
                    alert('Submission successful! Check your email.');
                    document.getElementById(`${sectionId}-name`).value = ''; // Clear name after success
                }, function(error) {
                    alert('Submission failed. Please check your internet connection or try again later.');
                    console.error('EmailJS Error:', error);
                });

            // Handle file attachment for conversation and speaking sections
            if ((sectionId === 'conversation' || sectionId === 'speaking') && document.getElementById(`${sectionId}-file`).files[0]) {
                const formData = new FormData();
                formData.append('to_email', "abolfazlabdollahi199@gmail.com");
                formData.append('from_name', nameInput);
                formData.append('message', message);
                formData.append('file', document.getElementById(`${sectionId}-file`).files[0]);

                fetch('https://api.emailjs.com/api/v1.0/email/send', {
                    method: 'POST',
                    body: formData
                })
                .then(response => response.json())
                .then(data => {
                    if (data.status === 'success') {
                        alert('File uploaded successfully!');
                    } else {
                        alert('File upload failed. Please try again.');
                    }
                })
                .catch(error => {
                    alert('Error uploading file. Check your internet connection.');
                    console.error('File Upload Error:', error);
                });
            }
        }

        // Add click event for rating buttons
        document.querySelectorAll('#review button[data-value]').forEach(button => {
            button.addEventListener('click', function() {
                this.style.backgroundColor = '#4F46E5';
                this.style.color = 'white';
                const siblings = this.parentElement.querySelectorAll('button');
                siblings.forEach(sib => {
                    if (sib !== this) {
                        sib.style.backgroundColor = '';
                        sib.style.color = '';
                    }
                });
            });
        });
    </script>
</body>
</html>
