<!-- Header.svelte -->
<script>
    // Define the navigation links for your top bar
    const navigationLinks = [
        { label: 'Home', route: '/' },
        { label: 'About', route: '/about' },
        { label: 'Services', route: '/services' },
        // Add more navigation links as needed
    ];

    // Function to handle link clicks
    function handleLinkClick(route) {
        // You can implement the navigation logic here
        console.log(`Navigating to ${route}`);
    }
</script>

<header class="top-bar">
    <nav class="navigation">
        <ul>
            {#each navigationLinks as link (link.label)}
                <li on:click={() => handleLinkClick(link.route)}>
                    <a href="javascript:void(0)">{link.label}</a>
                </li>
            {/each}
        </ul>
    </nav>
</header>

<style>
    /* Add your top bar styling here */
    .top-bar {
        background-color: #333;
        color: #fff;
        padding: 10px 20px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .navigation ul {
        list-style: none;
        padding: 0;
        display: flex;
    }

    .navigation li {
        margin-right: 20px;
        cursor: pointer;
    }

    .navigation a {
        text-decoration: none;
        color: #fff;
    }

    .navigation a:hover {
        text-decoration: underline;
    }
</style>
