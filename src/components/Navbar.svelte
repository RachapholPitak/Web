<script>
    import { page } from '$app/stores';
    const navs = [
        {
            title: "Home",
            href: "/"
        },
        {
            title: "About",
            href: "/about"
        },
        {
            title: "Service",
            href: "/service"
        },
        {
            title: "Contact",
            href: "/contact"
        },
    ]
    $: routeId = $page.route.id;
</script>
<div class="navbar bg-base-100">
    <div class="flex-1">
        <a class="btn btn-ghost normal-case text-xl">SmartDev</a>
    </div>
    <div class="flex-none">
        <ul class="menu menu-horizontal px-1">
            {#each navs as {title, href}}
                <li>
                    <a {href} class:active={routeId == href}>{title}</a>
                </li>
                
            {/each}    

        </ul>
      </div>
</div>