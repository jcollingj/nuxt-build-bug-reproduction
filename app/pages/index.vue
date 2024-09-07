<script setup lang="ts"></script>

<template>
  <div>
    <div class="w-full flex flex-row justify-center">
      <ULandingHero
        orientation="horizontal"
        :ui="{
          wrapper:
            'py-24 sm:py-32 md:py-40 relative flex items-center justify-center',
          container: 'gap-16 sm:gap-y-24 flex flex-col items-center',
          base: 'text-center',
          headline: 'mb-10',
          title:
            'text-5xl font-bold tracking-tight text-gray-900 dark:text-white sm:text-7xl',
          description:
            'mt-6 text-lg tracking-tight text-gray-600 dark:text-gray-300',
          links: 'mt-10 flex flex-wrap justify-center gap-x-6 gap-y-3',
        }"
      >
        <template #headline>
          <UBadge
            variant="subtle"
            size="lg"
            class="relative rounded-full font-semibold"
          >
            <NuxtLink
              to="/example-link"
              target="_blank"
              class="focus:outline-none"
              tabindex="-1"
            >
              <span class="absolute inset-0" aria-hidden="true"></span>
            </NuxtLink>

            Hey, 👋
          </UBadge>
        </template>
        <template #description>
          <p class="whitespace-pre-line">
            This is a sample description for the landing page. It can span
            multiple lines and provide a brief overview.
          </p>
        </template>

        <template #title>
          <h1>Welcome to Our Amazing Product</h1>
        </template>
      </ULandingHero>
    </div>

    <ULandingSection
      title="Our Features"
      :links="[{ label: 'Learn More', to: '/features' }]"
    >
      <UPageGrid>
        <ULandingCard
          title="Feature 1"
          description="Description of feature 1"
          icon="i-heroicons-rocket-launch"
        />
        <ULandingCard
          title="Feature 2"
          description="Description of feature 2"
          icon="i-heroicons-chart-bar"
        />
        <ULandingCard
          title="Feature 3"
          description="Description of feature 3"
          icon="i-heroicons-finger-print"
        />
      </UPageGrid>
    </ULandingSection>
  </div>
</template>
