<template>
  <main class="container">
    <div class="jumbotron text-center">
      <h1>Car Shop</h1>
      <p>Welcome to our new online car shop</p>
    </div>

    <article class="list-group">
      <section class="list-group-item">
        <!-- Add products here -->
      </section>
    </article>
  </main>
</template>

<script>
// remove when will be used
// eslint-disable-next-line no-unused-vars
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

  asyncData() {
    return {}
  }
}
</script>
