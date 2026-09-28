<template>
  <header class="w-full bg-[#001b5e] text-white">
    <div
      class="mx-auto flex h-14 max-w-7xl items-center justify-center px-4 sm:px-6 lg:px-8"
    >
      <div class="flex items-center gap-3 text-sm font-semibold">
        <!-- Email -->
        <a
          href="mailto:info@usea.edu.kh"
          class="flex items-center gap-1 transition-colors hover:text-gray-300"
        >
          <Icon name="lucide:mail" class="h-4 w-4" />

          <span>info@usea.edu.kh</span>
        </a>

        <!-- Divider -->
        <span class="text-white/70">|</span>

        <!-- Journal -->
        <a
          href="https://rj.usea.edu.kh"
          target="_blank"
          rel="noopener noreferrer"
          class="transition-colors hover:text-gray-300"
        >
          Journal
        </a>

        <!-- Divider -->
        <span class="text-white/70">|</span>

        <!-- LMS -->
        <a href="#" class="transition-colors hover:text-gray-300"> LMS </a>

        <!-- Divider -->
        <span class="text-white/70">|</span>

        <!-- Language -->
        <button
          type="button"
          class="flex items-center gap-1 transition-opacity hover:opacity-80"
          aria-label="Change language"
        >
          <Icon name="circle-flags:kh" class="h-5 w-5" />
        </button>
      </div>
    </div>
  </header>
</template>
