<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nababpur Business Finder</title>
    
    <!-- Tailwind CSS for styling -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Google Fonts: Inter -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">

    <style>
        /* Custom scrollbar for a better dark mode aesthetic */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #1a202c; /* gray-800 */
        }
        ::-webkit-scrollbar-thumb {
            background: #4a5568; /* gray-600 */
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #718096; /* gray-500 */
        }
        body {
            font-family: 'Inter', sans-serif;
        }
    </style>
</head>
<body class="bg-gray-900 text-gray-200 min-h-screen">

    <div class="container mx-auto p-4 md:p-8">
        
        <!-- Header -->
        <header class="text-center mb-8">
            <h1 class="text-4xl md:text-5xl font-bold text-cyan-400">Nababpur Business Finder</h1>
            <p class="text-gray-400 mt-2">Your guide to the hardware & electronics hub of Dhaka.</p>
        </header>

        <!-- Search Section -->
        <main>
            <div class="max-w-2xl mx-auto">
                <div class="relative">
                    <div class="absolute inset-y-0 left-0 pl-3 flex items-center pointer-events-none">
                        <svg class="h-5 w-5 text-gray-400" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor">
                            <path fill-rule="evenodd" d="M8 4a4 4 0 100 8 4 4 0 000-8zM2 8a6 6 0 1110.89 3.476l4.817 4.817a1 1 0 01-1.414 1.414l-4.816-4.816A6 6 0 012 8z" clip-rule="evenodd" />
                        </svg>
                    </div>
                    <input type="text" id="searchInput"
                           class="w-full bg-gray-800 border border-gray-700 text-gray-200 rounded-lg shadow-sm py-3 pl-10 pr-4 focus:outline-none focus:ring-2 focus:ring-cyan-500 transition duration-300"
                           placeholder="Search for products (e.g., LED bulb, water pump)...">
                    
                    <!-- Autocomplete Suggestions Container -->
                    <div id="suggestions" class="absolute z-10 w-full bg-gray-800 border border-gray-700 rounded-lg mt-1 shadow-lg hidden max-h-60 overflow-y-auto">
                        <!-- Suggestions will be populated by JavaScript -->
                    </div>
                </div>
            </div>

            <!-- Results Section -->
            <section id="results" class="mt-10 grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                <!-- Business cards will be populated by JavaScript -->
            </section>
        </main>
        
    </div>

    <script>
        // --- SAMPLE DATA ---
        // In a real application, this data would come from a database (like DynamoDB).
        // For GitHub Pages, we embed it directly in the JS.
        const businesses = [
            {
                id: 'haji-electronics',
                name: 'Haji Electronics',
                address: '27 Nawabpur Rd, Dhaka 1100',
                contact: '0171-XXX-XXXX',
                type: 'Electronics Store',
                products: ['LED bulbs', 'switches', 'wiring cables', 'fans', 'circuit breakers']
            },
            {
                id: 'bismillah-machinery',
                name: 'Bismillah Machinery',
                address: '145 Nawabpur Rd, Dhaka 1100',
                contact: '0182-XXX-XXXX',
                type: 'Machinery & Equipment',
                products: ['water pump', 'power tools', 'generators', 'drill machine', 'welding machine']
            },
            {
                id: 'national-electric',
                name: 'National Electric Co.',
                address: '155 Nawabpur Rd, Dhaka 1100',
                contact: 'N/A',
                type: 'Electrical Supply Store',
                products: ['industrial wiring', 'sockets', 'switches', 'conduit pipes', 'LED bulbs']
            },
            {
                id: 'golden-tools-hardware',
                name: 'Golden Tools & Hardware',
                address: '161 Nawabpur Rd, Dhaka 1100',
                contact: '0191-XXX-XXXX',
                type: 'Hardware Store',
                products: ['hand tools', 'screws', 'nuts and bolts', 'locks', 'power tools', 'drill machine']
            },
            {
                id: 'super-star-showroom',
                name: 'Super Star Group Showroom',
                address: '37 Nawabpur Rd, Dhaka 1100',
                contact: '0167-XXX-XXXX',
                type: 'Lighting & Fan Store',
                products: ['LED bulbs', 'tube lights', 'ceiling fans', 'exhaust fans', 'fancy lights']
            },
            {
                id: 'national-pump-machinery',
                name: 'National Pump & Machinery',
                address: '172 Nawabpur Rd, Dhaka 1100',
                contact: '0155-XXX-XXXX',
                type: 'Pump Supplier',
                products: ['submersible pump', 'water pump', 'pressure washer', 'industrial pumps']
            },
            {
                id: 'unique-paint-hardware',
                name: 'Unique Paint & Hardware',
                address: '182 Nawabpur Rd, Dhaka 1100',
                contact: 'N/A',
                type: 'Hardware & Paint Store',
                products: ['paints', 'brushes', 'hand tools', 'locks', 'door handles']
            },
             {
                id: 'yasin-machinery',
                name: 'Yasin Machinery',
                address: '148 Nawabpur Rd, Dhaka 1100',
                contact: '0173-XXX-XXXX',
                type: 'Industrial Machinery',
                products: ['lathe machine', 'welding machine', 'air compressor', 'power tools']
            }
        ];

        // --- DOM ELEMENT REFERENCES ---
        const searchInput = document.getElementById('searchInput');
        const resultsContainer = document.getElementById('results');
        const suggestionsContainer = document.getElementById('suggestions');

        // --- PREPARE DATA FOR AUTOCOMPLETE ---
        // Create a unique, flat list of all searchable terms (products and business names)
        const allProducts = businesses.flatMap(b => b.products);
        const allBusinessNames = businesses.map(b => b.name);
        const searchableItems = [...new Set([...allProducts, ...allBusinessNames])].sort();


        // --- EVENT LISTENERS ---
        searchInput.addEventListener('input', () => {
            const query = searchInput.value.toLowerCase();
            displayResults(query);
            showSuggestions(query);
        });

        // Hide suggestions when clicking outside
        document.addEventListener('click', (event) => {
            if (!searchInput.contains(event.target)) {
                suggestionsContainer.classList.add('hidden');
            }
        });

        // --- CORE FUNCTIONS ---

        /**
         * Renders autocomplete suggestions based on user input.
         * @param {string} query - The user's search input.
         */
        function showSuggestions(query) {
            if (!query) {
                suggestionsContainer.classList.add('hidden');
                return;
            }

            const filteredSuggestions = searchableItems.filter(item =>
                item.toLowerCase().includes(query)
            ).slice(0, 10); // Show max 10 suggestions

            if (filteredSuggestions.length === 0) {
                suggestionsContainer.classList.add('hidden');
                return;
            }
            
            suggestionsContainer.innerHTML = ''; // Clear old suggestions
            filteredSuggestions.forEach(item => {
                const div = document.createElement('div');
                div.textContent = item;
                div.className = 'p-3 hover:bg-gray-700 cursor-pointer text-gray-300';
                div.addEventListener('click', () => {
                    searchInput.value = item;
                    suggestionsContainer.classList.add('hidden');
                    displayResults(item.toLowerCase());
                });
                suggestionsContainer.appendChild(div);
            });
            suggestionsContainer.classList.remove('hidden');
        }

        /**
         * Filters businesses based on the search query and renders them.
         * @param {string} query - The user's search term.
         */
        function displayResults(query) {
            resultsContainer.innerHTML = ''; // Clear previous results

            if (!query) {
                resultsContainer.innerHTML = `<div class="col-span-full text-center text-gray-500"><p>Start by searching for a product or business name.</p></div>`;
                return;
            }

            const filteredBusinesses = businesses.filter(business => {
                const nameMatch = business.name.toLowerCase().includes(query);
                const productMatch = business.products.some(product => product.toLowerCase().includes(query));
                return nameMatch || productMatch;
            });

            if (filteredBusinesses.length === 0) {
                resultsContainer.innerHTML = `<div class="col-span-full text-center text-gray-500"><p>No businesses found matching "${searchInput.value}".</p></div>`;
                return;
            }

            filteredBusinesses.forEach(business => {
                const card = `
                    <div class="bg-gray-800 rounded-lg shadow-md p-6 border border-gray-700 transform hover:scale-105 transition-transform duration-300">
                        <h2 class="text-xl font-bold text-cyan-400">${business.name}</h2>
                        <p class="text-sm text-gray-400 mb-4">${business.type}</p>
                        <div class="space-y-2 text-gray-300">
                            <p><strong>Address:</strong> ${business.address}</p>
                            <p><strong>Contact:</strong> ${business.contact}</p>
                        </div>
                        <div class="mt-4">
                            <h4 class="font-semibold text-gray-400">Known For:</h4>
                            <div class="flex flex-wrap gap-2 mt-2">
                                ${business.products.map(product => `<span class="bg-gray-700 text-cyan-200 text-xs font-medium px-2.5 py-1 rounded-full">${product}</span>`).join('')}
                            </div>
                        </div>
                    </div>
                `;
                resultsContainer.innerHTML += card;
            });
        }
        
        // --- INITIAL RENDER ---
        // Display initial message on page load.
        displayResults('');

    </script>
</body>
</html>

