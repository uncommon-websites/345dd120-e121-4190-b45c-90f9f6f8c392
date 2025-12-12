<script>
  const logos = [
    { name: "Ultrasound Ireland", font: "font-sans font-bold" },
    { name: "RETAIL CO", font: "font-mono font-bold tracking-widest" },
    { name: "ServicePro", font: "font-sans font-bold" },
    { name: "CafeCentral", font: "font-serif font-bold text-xl" },
    { name: "CleanTeam", font: "font-sans font-bold italic" },
    { name: "FitLife Gyms", font: "font-sans font-bold" },
    { name: "SALON LUXE", font: "font-sans font-light uppercase tracking-widest" },
    { name: "TechFlow", font: "font-sans font-bold tracking-tight" },
    { name: "RestaurantHub", font: "font-sans font-bold" },
    { name: "CareCrew", font: "font-sans font-black tracking-tighter" },
    { name: "BuildRight", font: "font-sans font-bold" },
    { name: "ShopLocal", font: "font-serif italic font-bold" },
  ];
</script>

<section class="py-16 border-b border-gray-100">
  <div class="container-custom text-center">
    <p class="text-[10px] font-bold tracking-[0.2em] text-gray-400 uppercase mb-10">
      Over 1,000 service businesses trust CrewHR
    </p>
    
    <div class="grid grid-cols-2 md:grid-cols-4 lg:grid-cols-6 gap-x-8 gap-y-12 items-center justify-items-center opacity-60 grayscale hover:grayscale-0 transition-all duration-500">
      {#each logos as logo}
        <div class="text-xl md:text-2xl text-gray-800 flex items-center justify-center w-full">
           <!-- Placeholder for actual SVG logos -->
           <span class="{logo.font}">{logo.name}</span>
        </div>
      {/each}
    </div>
  </div>
</section>
