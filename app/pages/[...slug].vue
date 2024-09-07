<script setup lang="ts">
// No setup script needed for hard-coded content
</script>

<template>
  <UPage>
    <UPageHeader
      title="Sample Page Title"
      description="This is a sample page description"
      :links="[
        { label: 'Home', to: '/' },
        { label: 'About', to: '/about' },
      ]"
      headline="Welcome!"
    />

    <UPageBody prose>
      <h1>Sample Content</h1>
      <p>
        This is some sample content for testing purposes. It replaces the
        dynamic ContentRenderer.
      </p>

      <hr />

      <div>
        <h2>Navigation</h2>
        <ul>
          <li><a href="/prev-page">Previous Page</a></li>
          <li><a href="/next-page">Next Page</a></li>
        </ul>
      </div>
    </UPageBody>

    <template #right>
      <UContentToc
        title="Table of Contents"
        :links="[
          { id: 'section-1', text: 'Section 1', depth: 2 },
          { id: 'section-2', text: 'Section 2', depth: 2 },
          { id: 'subsection-2-1', text: 'Subsection 2.1', depth: 3 },
        ]"
      >
        <template #bottom>
          <div class="hidden lg:block space-y-6 !mt-6">
            <UDivider type="dashed" />

            <UPageLinks
              title="Related Links"
              :links="[
                { label: 'Link 1', to: '/link1' },
                { label: 'Link 2', to: '/link2' },
              ]"
            />
          </div>
        </template>
      </UContentToc>
    </template>
  </UPage>
</template>
