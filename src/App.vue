<script setup>
import { ref } from 'vue'

const copiedText = ref('')

const copyToClipboard = async (text) => {
  try {
    await navigator.clipboard.writeText(text)
    copiedText.value = text
    setTimeout(() => {
      copiedText.value = ''
    }, 2000)
  } catch (err) {
    console.error('Failed to copy', err)
  }
}
</script>

<template>
  <div class="min-h-screen bg-slate-50 dark:bg-slate-900 text-slate-900 dark:text-slate-50 font-sans selection:bg-blue-500 selection:text-white">
    <!-- Main Container -->
    <main class="max-w-5xl mx-auto px-6 py-16 sm:py-24 space-y-24 sm:space-y-32">
      
      <!-- Hero Section -->
      <section class="flex flex-col md:flex-row items-center text-center md:text-left justify-between gap-12">
        <div class="flex-1 space-y-6">
          <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-blue-100 dark:bg-blue-900/30 text-blue-700 dark:text-blue-300 text-sm font-medium">
            <i class='bx bx-map'></i>
            <span>Nairobi, Kenya</span>
          </div>
          <h1 class="text-4xl sm:text-5xl md:text-6xl font-bold tracking-tight text-slate-900 dark:text-white">
            Richard Thiongo
          </h1>
          <h2 class="text-xl sm:text-2xl font-medium text-slate-600 dark:text-slate-400">
            Software Developer
          </h2>
          <p class="text-base sm:text-lg text-slate-600 dark:text-slate-400 max-w-2xl leading-relaxed">
            I specialize in Frontend (React, Next, Vue) and Backend (Python). 
            I build robust, cross-platform mobile apps with React Native, and design seamless 
            database architectures using MySQL, PostgreSQL, and Supabase.
          </p>
          <div class="flex flex-wrap items-center justify-center md:justify-start gap-4 pt-4">
            <a href="mailto:thiongorichard0@gmail.com" class="inline-flex items-center gap-2 px-6 py-3 bg-blue-600 hover:bg-blue-700 text-white font-medium rounded-lg shadow-sm transition-colors">
              <i class='bx bx-envelope text-xl'></i>
              Email Me
            </a>
            <a href="https://github.com/richard-thiongo" target="_blank" rel="noopener noreferrer" class="inline-flex items-center gap-2 px-6 py-3 bg-slate-200 hover:bg-slate-300 dark:bg-slate-800 dark:hover:bg-slate-700 text-slate-900 dark:text-white font-medium rounded-lg shadow-sm transition-colors">
              <i class='bx bxl-github text-xl'></i>
              GitHub
            </a>
            <a href="https://wa.me/254142029498" target="_blank" rel="noopener noreferrer" class="inline-flex items-center gap-2 px-6 py-3 bg-green-600 hover:bg-green-700 text-white font-medium rounded-lg shadow-sm transition-colors">
              <i class='bx bxl-whatsapp text-xl'></i>
              WhatsApp
            </a>
          </div>
          <div class="pt-4 flex items-center justify-center md:justify-start gap-2 text-slate-500 dark:text-slate-400 text-sm font-medium">
            <i class='bx bx-briefcase'></i>
            <span>2 Years of Professional Experience</span>
          </div>
        </div>
        <div class="shrink-0">
          <div class="relative w-36 h-48 sm:w-48 sm:h-64 rounded-2xl p-1.5 bg-gradient-to-tr from-blue-500 to-purple-500 shadow-xl rotate-3 hover:rotate-0 transition-transform duration-300">
            <div class="w-full h-full rounded-xl overflow-hidden bg-slate-200 dark:bg-slate-800 border-4 border-white dark:border-slate-900">
              <img src="/avatar.jpg" alt="Richard Thiongo" class="w-full h-full object-cover" />
            </div>
          </div>
        </div>
      </section>

      <!-- Skills Section -->
      <section class="space-y-8">
        <h3 class="text-2xl font-bold text-slate-900 dark:text-white flex items-center gap-3 border-b border-slate-200 dark:border-slate-800 pb-4">
          <i class='bx bx-code-alt text-blue-500'></i>
          Technical Arsenal
        </h3>
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
          <!-- Frontend -->
          <div class="p-6 bg-white dark:bg-slate-800 rounded-2xl shadow-sm border border-slate-100 dark:border-slate-700">
            <div class="w-12 h-12 rounded-xl bg-blue-50 dark:bg-blue-900/20 flex items-center justify-center mb-4">
              <i class='bx bx-layout text-2xl text-blue-600 dark:text-blue-400'></i>
            </div>
            <h4 class="text-lg font-semibold mb-2">Frontend</h4>
            <ul class="space-y-2 text-slate-600 dark:text-slate-400">
              <li class="flex items-center gap-2"><i class='bx bxl-react'></i> React JS</li>
              <li class="flex items-center gap-2"><i class='bx bx-globe'></i> Next JS</li>
              <li class="flex items-center gap-2"><i class='bx bxl-vuejs'></i> Vue JS</li>
              <li class="flex items-center gap-2"><i class='bx bxl-css3'></i> Tailwind CSS</li>
            </ul>
          </div>
          <!-- Backend -->
          <div class="p-6 bg-white dark:bg-slate-800 rounded-2xl shadow-sm border border-slate-100 dark:border-slate-700">
            <div class="w-12 h-12 rounded-xl bg-purple-50 dark:bg-purple-900/20 flex items-center justify-center mb-4">
              <i class='bx bx-server text-2xl text-purple-600 dark:text-purple-400'></i>
            </div>
            <h4 class="text-lg font-semibold mb-2">Backend & DB</h4>
            <ul class="space-y-2 text-slate-600 dark:text-slate-400">
              <li class="flex items-center gap-2"><i class='bx bxl-python'></i> Python</li>
              <li class="flex items-center gap-2"><i class='bx bx-data'></i> MySQL</li>
              <li class="flex items-center gap-2"><i class='bx bxs-data'></i> PostgreSQL</li>
              <li class="flex items-center gap-2"><i class='bx bx-cloud'></i> Supabase</li>
            </ul>
          </div>
          <!-- Mobile -->
          <div class="p-6 bg-white dark:bg-slate-800 rounded-2xl shadow-sm border border-slate-100 dark:border-slate-700">
            <div class="w-12 h-12 rounded-xl bg-green-50 dark:bg-green-900/20 flex items-center justify-center mb-4">
              <i class='bx bx-mobile-alt text-2xl text-green-600 dark:text-green-400'></i>
            </div>
            <h4 class="text-lg font-semibold mb-2">Mobile</h4>
            <ul class="space-y-2 text-slate-600 dark:text-slate-400">
              <li class="flex items-center gap-2"><i class='bx bxl-react'></i> React Native</li>
              <li class="flex items-center gap-2"><i class='bx bxl-android'></i> Kotlin</li>
              <li class="flex items-center gap-2"><i class='bx bx-mobile'></i> Android Studio</li>
            </ul>
          </div>
          <!-- Tools -->
          <div class="p-6 bg-white dark:bg-slate-800 rounded-2xl shadow-sm border border-slate-100 dark:border-slate-700">
            <div class="w-12 h-12 rounded-xl bg-orange-50 dark:bg-orange-900/20 flex items-center justify-center mb-4">
              <i class='bx bx-wrench text-2xl text-orange-600 dark:text-orange-400'></i>
            </div>
            <h4 class="text-lg font-semibold mb-2">Tools</h4>
            <ul class="space-y-2 text-slate-600 dark:text-slate-400">
              <li class="flex items-center gap-2"><i class='bx bx-git-branch'></i> Git</li>
              <li class="flex items-center gap-2"><i class='bx bxl-github'></i> GitHub</li>
              <li class="flex items-center gap-2"><i class='bx bxl-css3'></i> CSS3</li>
            </ul>
          </div>
        </div>
      </section>

      <!-- Projects Section -->
      <section class="space-y-8">
        <h3 class="text-2xl font-bold text-slate-900 dark:text-white flex items-center gap-3 border-b border-slate-200 dark:border-slate-800 pb-4">
          <i class='bx bx-folder text-blue-500'></i>
          Featured Projects
        </h3>
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">

          <!-- Craft CV Project -->
          <div class="flex flex-col bg-white dark:bg-slate-800 rounded-2xl overflow-hidden shadow-sm border border-slate-100 dark:border-slate-700">
            <div class="aspect-video w-full bg-slate-200 dark:bg-slate-900 border-b border-slate-100 dark:border-slate-700 relative">
              <img src="https://image.thum.io/get/width/1000/crop/800/https://craft-cv-alpha.vercel.app/" alt="Craft CV Preview" class="w-full h-full object-cover" loading="lazy" />
            </div>
            <div class="p-6 flex flex-col flex-1">
              <h4 class="text-xl font-bold mb-2">Craft CV</h4>
              <p class="text-slate-600 dark:text-slate-400 mb-6 flex-1">A platform that allows users to generate professional CVs and resumes using AI, with intelligent content suggestions and clean formatting.</p>
              <a href="https://craft-cv-alpha.vercel.app/" target="_blank" rel="noopener noreferrer" class="inline-flex items-center justify-center gap-2 w-full px-4 py-2 bg-blue-50 dark:bg-blue-900/20 text-blue-700 dark:text-blue-400 font-medium rounded-lg hover:bg-blue-100 dark:hover:bg-blue-900/40 transition-colors">
                <i class='bx bx-link-external'></i> View Live Project
              </a>
            </div>
          </div>
          
          <!-- Project 1 -->
          <div class="flex flex-col bg-white dark:bg-slate-800 rounded-2xl overflow-hidden shadow-sm border border-slate-100 dark:border-slate-700">
            <div class="aspect-video w-full bg-slate-200 dark:bg-slate-900 border-b border-slate-100 dark:border-slate-700 relative">
              <img src="https://image.thum.io/get/width/1000/crop/800/https://exam-archive-nine.vercel.app/" alt="Exam Archive Preview" class="w-full h-full object-cover" loading="lazy" />
            </div>
            <div class="p-6 flex flex-col flex-1">
              <h4 class="text-xl font-bold mb-2">Exam Archive</h4>
              <p class="text-slate-600 dark:text-slate-400 mb-6 flex-1">A comprehensive archive for educational materials and past papers.</p>
              <a href="https://exam-archive-nine.vercel.app/" target="_blank" rel="noopener noreferrer" class="inline-flex items-center justify-center gap-2 w-full px-4 py-2 bg-blue-50 dark:bg-blue-900/20 text-blue-700 dark:text-blue-400 font-medium rounded-lg hover:bg-blue-100 dark:hover:bg-blue-900/40 transition-colors">
                <i class='bx bx-link-external'></i> View Live Project
              </a>
            </div>
          </div>

          <!-- Project 2 -->
          <div class="flex flex-col bg-white dark:bg-slate-800 rounded-2xl overflow-hidden shadow-sm border border-slate-100 dark:border-slate-700">
            <div class="aspect-video w-full bg-slate-200 dark:bg-slate-900 border-b border-slate-100 dark:border-slate-700 relative">
              <img src="https://image.thum.io/get/width/1000/crop/800/https://richard-honey.vercel.app/" alt="Richard Honey Preview" class="w-full h-full object-cover" loading="lazy" />
            </div>
            <div class="p-6 flex flex-col flex-1">
              <h4 class="text-xl font-bold mb-2">Richard Honey</h4>
              <p class="text-slate-600 dark:text-slate-400 mb-6 flex-1">A modern e-commerce landing page for a premium honey delivery service.</p>
              <a href="https://richard-honey.vercel.app/" target="_blank" rel="noopener noreferrer" class="inline-flex items-center justify-center gap-2 w-full px-4 py-2 bg-blue-50 dark:bg-blue-900/20 text-blue-700 dark:text-blue-400 font-medium rounded-lg hover:bg-blue-100 dark:hover:bg-blue-900/40 transition-colors">
                <i class='bx bx-link-external'></i> View Live Project
              </a>
            </div>
          </div>

          <!-- Project 3 -->
          <div class="flex flex-col bg-white dark:bg-slate-800 rounded-2xl overflow-hidden shadow-sm border border-slate-100 dark:border-slate-700">
            <div class="aspect-video w-full bg-slate-200 dark:bg-slate-900 border-b border-slate-100 dark:border-slate-700 relative">
              <img src="https://image.thum.io/get/width/1000/crop/800/https://sdms-web-two.vercel.app/" alt="SDMS Web Two Preview" class="w-full h-full object-cover" loading="lazy" />
            </div>
            <div class="p-6 flex flex-col flex-1">
              <h4 class="text-xl font-bold mb-2">SDMS Web Portal</h4>
              <p class="text-slate-600 dark:text-slate-400 mb-6 flex-1">A full-featured School Data Management System containing tailored portals for administrators, teachers, and students.</p>
              
              <div class="bg-slate-50 dark:bg-slate-900 rounded-xl p-4 mb-6 border border-slate-200 dark:border-slate-700 text-sm">
                <h5 class="font-semibold text-xs text-slate-500 uppercase tracking-wider mb-3"><i class='bx bx-key'></i> Test Credentials</h5>
                
                <div class="space-y-3">
                  <!-- Admin -->
                  <div>
                    <span class="text-[10px] font-bold text-slate-400 uppercase tracking-wider block mb-1">Admin</span>
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-2">
                      <div class="flex items-center justify-between gap-1 text-xs bg-white dark:bg-slate-800 px-2 py-1.5 rounded-md border border-slate-200 dark:border-slate-700">
                        <div class="flex items-center gap-1 overflow-hidden">
                          <i class='bx bx-envelope text-slate-400 shrink-0'></i>
                          <span class="font-mono text-slate-700 dark:text-slate-300 truncate">mzeethiongo@gmail.com</span>
                        </div>
                        <button @click="copyToClipboard('mzeethiongo@gmail.com')" class="text-slate-400 hover:text-blue-500 transition-colors shrink-0 p-0.5" title="Copy">
                          <i class='bx' :class="copiedText === 'mzeethiongo@gmail.com' ? 'bx-check text-green-500' : 'bx-copy'"></i>
                        </button>
                      </div>
                      <div class="flex items-center justify-between gap-1 text-xs bg-white dark:bg-slate-800 px-2 py-1.5 rounded-md border border-slate-200 dark:border-slate-700">
                        <div class="flex items-center gap-1 overflow-hidden">
                          <i class='bx bx-lock-alt text-slate-400 shrink-0'></i>
                          <span class="font-mono text-slate-700 dark:text-slate-300 truncate">I love it man !</span>
                        </div>
                        <button @click="copyToClipboard('I love it man !')" class="text-slate-400 hover:text-blue-500 transition-colors shrink-0 p-0.5" title="Copy">
                          <i class='bx' :class="copiedText === 'I love it man !' ? 'bx-check text-green-500' : 'bx-copy'"></i>
                        </button>
                      </div>
                    </div>
                  </div>
                  
                  <!-- Teacher -->
                  <div class="pt-2 border-t border-slate-200 dark:border-slate-800">
                    <span class="text-[10px] font-bold text-slate-400 uppercase tracking-wider block mb-1">Teacher</span>
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-2">
                      <div class="flex items-center justify-between gap-1 text-xs bg-white dark:bg-slate-800 px-2 py-1.5 rounded-md border border-slate-200 dark:border-slate-700">
                        <div class="flex items-center gap-1 overflow-hidden">
                          <i class='bx bx-envelope text-slate-400 shrink-0'></i>
                          <span class="font-mono text-slate-700 dark:text-slate-300 truncate">johndoe@gmail.com</span>
                        </div>
                        <button @click="copyToClipboard('johndoe@gmail.com')" class="text-slate-400 hover:text-blue-500 transition-colors shrink-0 p-0.5" title="Copy">
                          <i class='bx' :class="copiedText === 'johndoe@gmail.com' ? 'bx-check text-green-500' : 'bx-copy'"></i>
                        </button>
                      </div>
                      <div class="flex items-center justify-between gap-1 text-xs bg-white dark:bg-slate-800 px-2 py-1.5 rounded-md border border-slate-200 dark:border-slate-700">
                        <div class="flex items-center gap-1 overflow-hidden">
                          <i class='bx bx-lock-alt text-slate-400 shrink-0'></i>
                          <span class="font-mono text-slate-700 dark:text-slate-300 truncate">I love it man !</span>
                        </div>
                        <button @click="copyToClipboard('I love it man !')" class="text-slate-400 hover:text-blue-500 transition-colors shrink-0 p-0.5" title="Copy">
                          <i class='bx' :class="copiedText === 'I love it man !' ? 'bx-check text-green-500' : 'bx-copy'"></i>
                        </button>
                      </div>
                    </div>
                  </div>

                  <!-- Student -->
                  <div class="pt-2 border-t border-slate-200 dark:border-slate-800">
                    <span class="text-[10px] font-bold text-slate-400 uppercase tracking-wider block mb-1">Student</span>
                    <div class="grid grid-cols-1 sm:grid-cols-3 gap-2">
                      <div class="flex items-center justify-between gap-1 text-xs bg-white dark:bg-slate-800 px-2 py-1.5 rounded-md border border-slate-200 dark:border-slate-700">
                        <div class="flex items-center gap-1 overflow-hidden">
                          <i class='bx bx-user text-slate-400 shrink-0'></i>
                          <span class="font-mono text-slate-700 dark:text-slate-300 truncate">Manu</span>
                        </div>
                        <button @click="copyToClipboard('Manu')" class="text-slate-400 hover:text-blue-500 transition-colors shrink-0 p-0.5" title="Copy">
                          <i class='bx' :class="copiedText === 'Manu' ? 'bx-check text-green-500' : 'bx-copy'"></i>
                        </button>
                      </div>
                      <div class="flex items-center justify-between gap-1 text-xs bg-white dark:bg-slate-800 px-2 py-1.5 rounded-md border border-slate-200 dark:border-slate-700">
                        <div class="flex items-center gap-1 overflow-hidden">
                          <i class='bx bx-user text-slate-400 shrink-0'></i>
                          <span class="font-mono text-slate-700 dark:text-slate-300 truncate">Kato</span>
                        </div>
                        <button @click="copyToClipboard('Kato')" class="text-slate-400 hover:text-blue-500 transition-colors shrink-0 p-0.5" title="Copy">
                          <i class='bx' :class="copiedText === 'Kato' ? 'bx-check text-green-500' : 'bx-copy'"></i>
                        </button>
                      </div>
                      <div class="flex items-center justify-between gap-1 text-xs bg-white dark:bg-slate-800 px-2 py-1.5 rounded-md border border-slate-200 dark:border-slate-700">
                        <div class="flex items-center gap-1 overflow-hidden">
                          <i class='bx bx-id-card text-slate-400 shrink-0'></i>
                          <span class="font-mono text-slate-700 dark:text-slate-300 truncate">8814</span>
                        </div>
                        <button @click="copyToClipboard('8814')" class="text-slate-400 hover:text-blue-500 transition-colors shrink-0 p-0.5" title="Copy">
                          <i class='bx' :class="copiedText === '8814' ? 'bx-check text-green-500' : 'bx-copy'"></i>
                        </button>
                      </div>
                    </div>
                  </div>
                </div>
              </div>

              <a href="https://sdms-web-two.vercel.app/" target="_blank" rel="noopener noreferrer" class="inline-flex items-center justify-center gap-2 w-full px-4 py-2 bg-blue-50 dark:bg-blue-900/20 text-blue-700 dark:text-blue-400 font-medium rounded-lg hover:bg-blue-100 dark:hover:bg-blue-900/40 transition-colors">
                <i class='bx bx-link-external'></i> View Live Project
              </a>
            </div>
          </div>

          <!-- Organic Precisions Project -->
          <div class="flex flex-col bg-white dark:bg-slate-800 rounded-2xl overflow-hidden shadow-sm border border-slate-100 dark:border-slate-700">
            <div class="aspect-video w-full bg-slate-200 dark:bg-slate-900 border-b border-slate-100 dark:border-slate-700 relative">
              <img src="https://image.thum.io/get/width/1000/crop/800/https://organic-precisions.vercel.app/" alt="Organic Precisions Preview" class="w-full h-full object-cover" loading="lazy" />
            </div>
            <div class="p-6 flex flex-col flex-1">
              <h4 class="text-xl font-bold mb-2">Organic Precisions</h4>
              <p class="text-slate-600 dark:text-slate-400 mb-6 flex-1">A sleek and modern Shop Management System tailored to streamline retail inventory, track sales transactions, and simplify business management.</p>
              
              <div class="bg-slate-50 dark:bg-slate-900 rounded-xl p-4 mb-6 border border-slate-200 dark:border-slate-700 text-sm">
                <h5 class="font-semibold text-xs text-slate-500 uppercase tracking-wider mb-3"><i class='bx bx-key'></i> Test Credentials</h5>
                
                <div class="space-y-3">
                  <div>
                    <span class="text-[10px] font-bold text-slate-400 uppercase tracking-wider block mb-1">Access PIN</span>
                    <div class="flex items-center justify-between gap-1 text-xs bg-white dark:bg-slate-800 px-3 py-1.5 rounded-md border border-slate-200 dark:border-slate-700">
                      <div class="flex items-center gap-2 overflow-hidden">
                        <i class='bx bx-lock-alt text-slate-400 shrink-0'></i>
                        <span class="font-mono text-slate-700 dark:text-slate-300 truncate">1900</span>
                      </div>
                      <button @click="copyToClipboard('1900')" class="text-slate-400 hover:text-blue-500 transition-colors shrink-0 p-0.5" title="Copy PIN">
                        <i class='bx' :class="copiedText === '1900' ? 'bx-check text-green-500' : 'bx-copy'"></i>
                      </button>
                    </div>
                  </div>
                </div>
              </div>

              <a href="https://organic-precisions.vercel.app/" target="_blank" rel="noopener noreferrer" class="inline-flex items-center justify-center gap-2 w-full px-4 py-2 bg-blue-50 dark:bg-blue-900/20 text-blue-700 dark:text-blue-400 font-medium rounded-lg hover:bg-blue-100 dark:hover:bg-blue-900/40 transition-colors">
                <i class='bx bx-link-external'></i> View Live Project
              </a>
            </div>
          </div>

        </div>
      </section>
      
      <!-- Footer -->
      <footer class="pt-8 border-t border-slate-200 dark:border-slate-800 text-center text-slate-500 dark:text-slate-400">
        <p>© 2026 Richard Thiongo. Built with Vue & Tailwind CSS.</p>
      </footer>

    </main>
  </div>
</template>

<style>
/* Any custom overrides can go here, but Tailwind is doing the heavy lifting */
</style>
