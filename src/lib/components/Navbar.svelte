<script>
  import { onMount } from 'svelte';
  
  let isScrolled = false;

  onMount(() => {
    const handleScroll = () => {
      isScrolled = window.scrollY > 10;
    };
    window.addEventListener('scroll', handleScroll);
    return () => window.removeEventListener('scroll', handleScroll);
  });
</script>

<nav class="fixed top-0 left-0 right-0 z-50 transition-all duration-300 {isScrolled ? 'bg-white/90 backdrop-blur-md border-b border-gray-100 py-3' : 'bg-transparent py-5'}">
  <div class="container-custom flex items-center justify-between">
    <div class="flex items-center gap-8">
      <a href="/" class="flex items-center gap-2 text-xl font-bold tracking-tight text-gray-900">
        <!-- Logo Icon -->
        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="text-plain-green">
          <path d="M20 7h-4V4c0-1.1-.9-2-2-2h-4c-1.1 0-2 .9-2 2v3H4c-1.1 0-2 .9-2 2v11c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V9c0-1.1-.9-2-2-2zM10 4h4v3h-4V4zm10 16H4V9h16v11z" fill="currentColor"/>
          <path d="M8 12h2v2H8zm0 4h2v2H8zm4-4h2v2h-2zm0 4h2v2h-2zm4-4h2v2h-2z" fill="currentColor"/>
        </svg>
        CrewHR
      </a>
      
      <div class="hidden md:flex items-center gap-6 text-sm font-medium text-gray-600">
        <a href="#features" class="hover:text-gray-900 transition-colors">Features</a>
        <a href="#pricing" class="hover:text-gray-900 transition-colors">Pricing</a>
        <a href="#customers" class="hover:text-gray-900 transition-colors">Customers</a>
        <a href="#" class="hover:text-gray-900 transition-colors">Resources <span class="text-xs ml-0.5">▼</span></a>
        <a href="#" class="hover:text-gray-900 transition-colors">Support</a>
      </div>
    </div>

    <div class="flex items-center gap-3">
      <a href="#" class="px-3 py-1.5 text-xs font-semibold border border-gray-200 rounded text-gray-700 hover:border-gray-400 transition-colors uppercase tracking-wide">
        Sign In
      </a>
      <a href="#" class="px-3 py-1.5 text-xs font-semibold bg-plain-green text-white rounded hover:opacity-90 transition-opacity uppercase tracking-wide">
        Start Free Trial
      </a>
    </div>
  </div>
</nav>
