<template>
  <nav class="bg-primary bg-theme sticky top-16 z-40 px-4">
    <div class="mx-auto max-w-screen-xl h-16 flex items-center justify-between text-sm">
      <!-- Header3만 고정 할 때 사용-->
      <!-- <header class="sticky top-0 z-50">
          <nav class="bg-white shadow">
            <div class="mx-auto max-w-screen-xl h-14 flex items-center justify-between text-sm text-gray-800"
            > -->
      <div class="md:w-1/2 w-auto flex flex-wrap justify-center gap-4">
        <NuxtLink to="/bible/memory" class="flex items-center gap-1 hover:underline">
          <BookOpenIcon class="w-5 h-5 nav-icon" />
          <span class="nav-label">오늘의 말씀</span>
        </NuxtLink>
        <NuxtLink to="/bible/qt" class="flex items-center gap-1 hover:underline">
          <ClipboardDocumentListIcon class="w-5 h-5 nav-icon" />
          <span class="nav-label">오늘의 QT</span>
        </NuxtLink>
        <NuxtLink to="/bible/reading" class="flex items-center gap-1 hover:underline">
          <BookmarkSquareIcon class="w-5 h-5 nav-icon" />
          <span class="nav-label">성경통독</span>
        </NuxtLink>
        <NuxtLink to="/bible/prayer" class="flex items-center gap-1 hover:underline">
          <ChatBubbleLeftRightIcon class="w-5 h-5 nav-icon" />
          <span class="nav-label">보혈 선포 기도문</span>
        </NuxtLink>
      </div>
      <div class="ml-auto flex items-center gap-4">
        <NuxtLink to="/auth/login" class="flex items-center gap-1 hover:underline">
          <ArrowRightOnRectangleIcon class="w-5 h-5 nav-icon" />
          <span class="nav-label">로그인</span>
        </NuxtLink>

        <NuxtLink to="/auth/signup" class="flex items-center gap-1 hover:underline">
          <UserPlusIcon class="w-5 h-5 nav-icon" />
          <span class="nav-label">회원가입</span>
        </NuxtLink>

        <NuxtLink to="/auth/profile" class="flex items-center gap-1 hover:underline">
          <UserIcon class="w-5 h-5 nav-icon" />
          <span class="nav-label">마이페이지</span>
        </NuxtLink>

        <form @submit.prevent class="search-field relative">
          <input
            type="text"
            placeholder="검색"
            class="pl-3 pr-10 py-1 border rounded text-sm focus:outline-none focus:ring-2 focus:ring-blue-500"
          />
          <button type="submit" class="absolute right-2 top-1/2 -translate-y-1/2">
            <MagnifyingGlassIcon class="w-5 h-5" />
          </button>
        </form>
      </div>
    </div>
  </nav>
</template>

<script setup lang="ts">
import {
  BookOpenIcon,
  ClipboardDocumentListIcon,
  BookmarkSquareIcon,
  ChatBubbleLeftRightIcon,
  ArrowRightOnRectangleIcon,
  UserPlusIcon,
  UserIcon,
  MagnifyingGlassIcon,
} from '@heroicons/vue/24/outline'
</script>

<style scoped>
/* 모바일: 아이콘 보임, 텍스트 숨김 */
.nav-icon {
  display: inline-block;
}
.nav-label {
  display: none;
}
.search-field {
  display: none;
}

/* 데스크톱(≥768px): 아이콘 숨김, 텍스트 보임 */
@media (min-width: 768px) {
  .nav-icon {
    display: none;
  }
  .nav-label {
    display: inline;
  }
  .search-field {
    display: flex;
  }
}
</style>
