<script>
    import router from "page";
    import { page, params } from './stores/pages.js';
    import Home from './pages/Home.svelte';
    import About from './pages/About.svelte';
    import Contact from './pages/Contact.svelte';
    import Donation from './pages/Donation.svelte';
    import NotFound from './pages/NotFound.svelte';
    import Success from './pages/Success.svelte';
    import Failure from './pages/Failure.svelte';

<<<<<<< HEAD
    
    router("/", () => ($page = Home));
    router("/about", () => ($page = About));
    router("/contact", () => ($page = Contact));
    router("/success", () => ($page = Success));
    router("/error" , () => ($page = Failure));
    router(
        "/donation/:id", 
        (ctx, next) => {
            $params = ctx.params;
            next();
        },
        () => ($page = Donation)
=======
    let page, params;

   
    router("/", () => (page = Home));
    router("/about", () => (page = About));
    router("/contact", () => (page = Contact));
    router("/success", () => (page = Success));
    router("/error", () => (page = Failure));
    router(
        "/donation/:id", 
        (ctx, next) => {
        params = ctx.params;
        next();
    },
    () => (page = Donation)
>>>>>>> 760f787bf414e6c16069cb515ea33fad0a0cdc5a
    );
    router('/*', () => ($page = NotFound));

    router.start();
</script>

<<<<<<< HEAD
<svelte:component this={$page} />
=======
<svelte:component this={page} {params} />


 
>>>>>>> 760f787bf414e6c16069cb515ea33fad0a0cdc5a
