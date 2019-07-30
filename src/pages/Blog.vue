<template>
  <Layout>
    <div v-for="edge in $page.posts.edges" :key="edge.node.title">
      <h2>{{ edge.node.title }}</h2>
      <p>{{ edge.node.excerpt }}</p>
    </div>
  </Layout>
</template>

<page-query>
query Posts {
    posts: allPost {
      edges {
        node {       
          title
          excerpt       
        }
      }
    }
  }
</page-query>