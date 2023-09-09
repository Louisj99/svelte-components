<!-- Sidebar.svelte -->
<script>
    // Define the items in your sidebar
    const sidebarItems = [
        { label: 'Home', icon: 'home', route: '/' },
        { label: 'About', icon: 'info', route: '/about' },
        { label: 'Services', icon: 'settings', route: '/services' },
        // Add more sidebar items as needed
    ];

    // Function to handle item click
    function handleItemClick(route) {
        // You can implement the navigation logic here
        console.log(`Navigating to ${route}`);
    }
</script>

<nav class="sidebar">
    <ul>
        {#each sidebarItems as item (item.label)}
            <li on:click={() => handleItemClick(item.route)}>
                <i class="material-icons">{item.icon}</i>
                <span>{item.label}</span>
            </li>
        {/each}
    </ul>
</nav>

<style>
    /* Add your sidebar styling here */
    .sidebar {
        width: 250px;
        background-color: #333;
        color: #fff;
        padding: 20px;
    }

    ul {
        list-style: none;
        padding: 0;
    }

    li {
        display: flex;
        align-items: center;
        padding: 10px;
        cursor: pointer;
        transition: background-color 0.3s ease;
    }

    li:hover {
        background-color: #555;
    }

    i {
        margin-right: 10px;
    }
</style>
