<script>
  // Define your social links here
  const socialLinks = [
    { name: "Twitter/ X", url: "https://twitter.com/yourusername", icon: "twitter" },
    { name: "Instagram", url: "https://instagram.com/yourusername", icon: "instagram" },
    // { name: "GitHub", url: "https://github.com/yourusername", icon: "github" }, // Replace with your URL
    // { name: "Twitter/ X", url: "https://twitter.com/yourusername", icon: "twitter" }, // Replace with your URL
    // { name: "LinkedIn", url: "https://linkedin.com/in/yourusername", icon: "linkedin" }, // Replace with your URL
    // { name: "Instagram", url: "https://instagram.com/yourusername", icon: "instagram" }, // Replace with your URL
    // Add more links as needed
  ];
</script>

<main>
  <div class="profile-container">
    <!-- Reference the image directly from the public folder -->
    <img src="/logo_hk.svg" alt="Profile Picture" class="profile-pic" /> 
    <h1>Lets connect</h1>
    <p class="subtitle">Harikrishnan Here</p> <!-- Added class and moved -->
    <ul class="links-list">
      {#each socialLinks as link}
        <li>
          <a href={link.url} target="_blank" rel="noopener noreferrer" class="link-button {link.icon}">
            {link.name}
          </a>
        </li>
      {/each}
    </ul>
  </div>
</main>

<style>
  main {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    min-height: 100vh; /* Ensure it takes full viewport height */
    padding: 1rem;
  }

  .profile-container {
    text-align: center;
  }

  .profile-pic {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    margin-bottom: 1rem;
    background-color: #444; /* Placeholder background */
    display: inline-block;
  }

  h1 {
    /* Reduced bottom margin to bring subtitle closer */
    margin-bottom: 0.5rem; 
    font-size: 2em;
    color: #e0e0e0; /* Lighter text color for dark mode */
  }

  /* Added styles for the subtitle */
  .subtitle {
    font-size: 1.1em;
    color: #b0b0b0; /* Slightly dimmer color than h1 */
    margin-bottom: 2rem; /* Add space before the links */
    font-weight: 300; /* Lighter font weight */
  }

  .links-list {
    list-style: none;
    padding: 0;
    margin: 0;
    width: 100%;
    max-width: 400px; /* Limit width of the links list */
  }

  .links-list li {
    margin-bottom: 1rem;
  }

  .link-button {
    display: block;
    padding: 1rem;
    background-color: #333; /* Darker button background */
    color: #f0f0f0; /* Light button text */
    text-decoration: none;
    border-radius: 8px;
    transition: background-color 0.3s ease, transform 0.2s ease;
    font-weight: 500;
  }

  .link-button:hover {
    background-color: #444; /* Slightly lighter on hover */
    transform: translateY(-2px);
  }

  /* Optional: Add specific styles or icons based on class names (e.g., .github, .twitter) */
  /* Example for GitHub button */
  .link-button.github {
    /* background-color: #2dba4e; /* Example GitHub green */
    /* You could add icons using ::before pseudo-elements and icon fonts/SVGs */
  }

</style>
