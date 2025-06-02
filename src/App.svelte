<script>
  // Define your social links here
  const socialLinks = [
    // Update icon property to point to the actual SVG file in the public folder
    { name: "Twitter/ X", url: "https://x.com/imharihk", icon: "/x_logo.svg" }, 
    { name: "Instagram", url: "https://www.instagram.com/harihk_/", icon: "/instagram_logo_dark.svg" },
    { name: "chess.com", url: "https://link.chess.com/friend/9YHSlm", icon: "/chess_com_logo.svg" },
    // { name: "GitHub", url: "https://github.com/yourusername", icon: "github" }, // Replace with your URL
    // { name: "LinkedIn", url: "https://linkedin.com/in/yourusername", icon: "linkedin" }, // Replace with your URL
    // Add more links as needed
  ];
</script>

<main class="flex flex-col items-center justify-center min-h-screen p-4 bg-gradient-to-br from-slate-900 via-gray-800 to-slate-900">
  <div class="text-center p-8 sm:p-10 bg-slate-700/40 backdrop-blur-md rounded-xl shadow-2xl max-w-lg w-full">
    <!-- Reference the image directly from the public folder -->
    <img src="/logo_hk.svg" alt="Profile Picture" class="w-36 h-36 rounded-full mb-6 border-[3px] border-slate-500 object-cover mx-auto" />
    <h1 class="mb-4 text-4xl sm:text-5xl text-slate-100 font-semibold">Let's connect</h1>
    <p class="text-lg sm:text-xl text-slate-300 mb-10 font-normal">Harikrishnan Here</p>
    <ul class="list-none p-0 mx-auto w-full max-w-md">
      {#each socialLinks as link}
        <li class="mb-5">
          <a href={link.url} target="_blank" rel="noopener noreferrer" class="flex items-center justify-center py-3 px-6 bg-slate-700/70 text-slate-100 no-underline rounded-full transition-all ease-in-out duration-300 font-medium border border-slate-600 hover:bg-gradient-to-r hover:from-sky-500 hover:to-indigo-600 hover:border-transparent hover:text-white hover:-translate-y-1 hover:shadow-xl transform">
            <!-- Add img tag for the logo -->
            <img src={link.icon} alt="{link.name} logo" class="w-5 h-5 mr-3" />
            {link.name}
          </a>
        </li>
      {/each}
    </ul>
  </div>
</main>

<style>
  /* All styles moved to Tailwind utility classes */
</style>
