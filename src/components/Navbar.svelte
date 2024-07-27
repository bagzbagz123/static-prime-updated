<script>
  import { onMount } from 'svelte';

  let menuVisible = false;

  const anchors = Array(100).fill(0).map((_, index) => index);

  function handleAnchorClick(event) {
      event.preventDefault();
      const link = event.currentTarget;
      const anchorId = new URL(link.href).hash.replace('#', '');
      const anchor = document.getElementById(anchorId);
      window.scrollTo({
          top: anchor.offsetTop,
          behavior: 'smooth'
      });
      menuVisible = false;  // Close menu after clicking a link
  }
</script>

<!-- Announcement Banner -->
<div class="bg-gradient-to-r ">
    <div class="max-w-[85rem] px-4 py-4 sm:px-6 lg:px-8 mx-auto">
      <!-- Grid -->
      <div class="grid justify-center md:grid-cols-2 md:justify-between md:items-center gap-2">
        <div class="text-center md:text-start md:order-2 md:flex md:justify-end md:items-center">
          <a class="py-2 px-3 mx-1  inline-flex items-center gap-x-2 text-sm font-semibold rounded-lg  text-black hover:border-black/70 hover:text-black/70 disabled:opacity-50 disabled:pointer-events-none" href="#Services">
            About us
          </a>
          <a class="py-2  mx-1 px-3 inline-flex items-center gap-x-2 text-sm font-semibold rounded-lg  text-black hover:border-black/70 hover:text-black/70 disabled:opacity-50 disabled:pointer-events-none" href="#Services">
            Services
          </a>
    
        </div>
        <!-- End Col -->
  
        <div class="flex items-center">
          <a class="py-2 px-3 inline-flex justify-center items-center gap-2 rounded-lg font-medium text-black hover:bg-black/10 focus:outline-none focus:ring-2 focus:ring-blue-600 focus:ring-offset-2 transition-all text-sm" href="#">
            <img class='w-10' src="static/primecapturelogo.png" alt="">
          </a>
          <span class="inline-block border-e border-black/30 w-px h-5 mx-2"></span>
          <a class="py-2 px-3 inline-flex justify-center items-center gap-2 rounded-lg font-medium text-black hover:bg-black/10 focus:outline-none focus:ring-2 focus:ring-blue-600 focus:ring-offset-2 transition-all text-sm" href="#">
            Prime Captures
          </a>
        </div>
        <!-- End Col -->
      </div>
      <!-- End Grid -->
    </div>
  </div>
  <!-- End Announcement Banner -->