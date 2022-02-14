<script>
<<<<<<< HEAD
	import CharityList from "../components/CharityList.svelte";
	import Header from '../components/Header.svelte';
	import Welcome from '../components/Welcome.svelte';
	import Promo from '../components/Promo.svelte';
	import Footer from '../components/Footer.svelte';
	import Loader from '../components/Loader.svelte';
=======
import CharityList from "../components/CharityList.svelte";
import Header from '../components/Header.svelte';
import Welcome from '../components/Welcome.svelte';
import Promo from '../components/Promo.svelte';
import Footer from '../components/Footer.svelte';
import Loader from "../components/Loader.svelte";

>>>>>>> 760f787bf414e6c16069cb515ea33fad0a0cdc5a

  let title = "Charity";
  let data = getData();
  
<<<<<<< HEAD
  <Header />
  <Welcome />

  <CharityList />
  <Promo />
  <Footer />
=======
 async function getData() {
      const res = await fetch('https://charity-api-bwa.herokuapp.com/charities');
      const data = await res.json();

      if(res.ok) {
         return data;
      } else {
          throw new Error(data);
      }
    }

</script>
  
<Header />
<Welcome />
{#await data}
<Loader />
{:then charities}
<CharityList {charities} />
{/await}
<Promo />
<Footer />
>>>>>>> 760f787bf414e6c16069cb515ea33fad0a0cdc5a
