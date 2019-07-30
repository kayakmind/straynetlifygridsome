<template>
  <Layout>
    <div v-for="edge in $page.posts.edges" :key="edge.node.title">
      {{ edge.node.title }}
      {{ edge.node.excerpt }}
    </div>
  </Layout>
</template>

<page-query>
query Posts {
    posts: allPost {
      edges {
        node {       
          title        
        }
      }
    }
  }
</page-query>