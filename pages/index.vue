<template>
  <main class="container">
    <div class="jumbotron text-center">
      <h1>Car Shop</h1>
      <p>Welcome to our new online car shop</p>
    </div>

    <article class="list-group">
      <section
        v-for="product in products"
        :key="product.id"
        class="list-group-item"
      >
        <h2>{{ product.name }}</h2>
      </section>
    </article>
  </main>
</template>

<script>
const getProducts = () => {
  return Promise.resolve([
    {
      id: 'car0',
      name: 'Opel Corsa B'
    },
    {
      id: 'car1',
      name: 'Opel Astra G'
    },
    {
      id: 'car2',
      name: 'Audi a3 p1'
    },
    {
      id: 'car3',
      name: 'Volkswagen Golf V'
    }
  ])
}

export default {
  name: 'HomePage',

  async asyncData() {
    return {
      products: await getProducts()
    }
  }
}
</script>
