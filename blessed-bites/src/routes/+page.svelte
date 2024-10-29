<script lang="ts">
  import { type MenuItem } from "$lib/types/MenuItem";
  const menuItems: MenuItem[] = [
    {
      name: "Grilled Chicken",
      img: "/images/grilled-chicken.jpg", // Make sure to replace with actual image paths
      price: 12.99,
      description: "Delicious grilled chicken with a side of veggies.",
    },
    {
      name: "Vegan Burger",
      img: "/images/vegan-burger.jpg",
      price: 10.99,
      description: "A tasty plant-based burger.",
    },
    // Add more items as needed
  ];
</script>

<page>
  <div class="container">
    <div class="row">
      <!-- Side Tab Navigation -->
      <div class="col s3">
        <ul class="collection with-header">
          <li class="collection-header"><h5>Menu Categories</h5></li>
          <li class="collection-item">Appetizers</li>
          <li class="collection-item">Main Dishes</li>
          <li class="collection-item">Desserts</li>
          <li class="collection-item">Drinks</li>
        </ul>
      </div>

      <!-- Main Menu Display -->
      <div class="col s9">
        <div class="row">
          {#each menuItems as item}
            <div class="col s12 m6 l4">
              <div class="card">
                <div class="card-image">
                  <img src={item.img} alt={item.name} />
                  <span class="card-title">{item.name}</span>
                </div>
                <div class="card-content">
                  <p>{item.description}</p>
                  <p class="price">{item.price}</p>
                </div>
              </div>
            </div>
          {/each}
        </div>
      </div>
    </div>
  </div>
</page>
