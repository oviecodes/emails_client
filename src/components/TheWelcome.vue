<script setup>
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import SupportIcon from './icons/IconSupport.vue'
</script>

<template>
  <WelcomeItem>
    <template #icon>
      <DocumentationIcon />
    </template>
    <template #heading>Vision</template>

    Lorem, ipsum dolor sit amet consectetur adipisicing elit. Voluptatibus corrupti eveniet asperiores assumenda, sit quia eligendi porro exercitationem! Vitae ab veniam dolorum voluptates! Iste rerum molestiae nobis tenetur unde odit.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <ToolingIcon />
    </template>
    <template #heading>Purpose</template>

    Lorem, ipsum dolor sit amet consectetur adipisicing elit. Alias optio, facere velit officiis dolore doloremque ipsa minima, explicabo, fugiat placeat debitis repellat. Assumenda accusantium enim, aspernatur nemo illo ducimus quia.

    <br />
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <EcosystemIcon />
    </template>
    <template #heading>Ecosystem</template>

    Lorem, ipsum dolor sit amet consectetur adipisicing elit. Architecto beatae officia culpa animi quas labore! Ducimus tempora, voluptatibus illo laudantium laborum repudiandae tempore labore fugit at excepturi dolore placeat minus?
  </WelcomeItem>

  <!-- <WelcomeItem>
    <template #icon>
      <CommunityIcon />
    </template>
    <template #heading>Community</template>

    Got stuck? Ask your question on
    <a target="_blank" href="https://chat.vuejs.org">Vue Land</a>, our official Discord server, or
    <a target="_blank" href="https://stackoverflow.com/questions/tagged/vue.js">StackOverflow</a>.
    You should also subscribe to
    <a target="_blank" href="https://news.vuejs.org">our mailing list</a> and follow the official
    <a target="_blank" href="https://twitter.com/vuejs">@vuejs</a>
    twitter account for latest news in the Vue world.
  </WelcomeItem> -->

  <!-- <WelcomeItem>
    <template #icon>
      <SupportIcon />
    </template>
    <template #heading>Support Vue</template>

    As an independent project, Vue relies on community backing for its sustainability. You can help
    us by
    <a target="_blank" href="https://vuejs.org/sponsor/">becoming a sponsor</a>.
  </WelcomeItem> -->
</template>
