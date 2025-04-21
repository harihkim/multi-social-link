<script>
  // Define your social links here
  const socialLinks = [
    { name: "Twitter/ X", url: "https://twitter.com/yourusername", icon: "twitter" },
    { name: "Instagram", url: "https://instagram.com/yourusername", icon: "instagram" },
    // { name: "GitHub", url: "https://github.com/yourusername", icon: "github" }, // Replace with your URL
    // { name: "LinkedIn", url: "https://linkedin.com/in/yourusername", icon: "linkedin" }, // Replace with your URL
    // Add more links as needed
  ];
</script>

<main>
  <div class="profile-container">
    <!-- Reference the image directly from the public folder -->
    <img src="/logo_hk.svg" alt="Profile Picture" class="profile-pic" />
    <h1>Let's connect</h1>
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
  /* Styles now align with the dark blue theme from app.css */
  main {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    min-height: 100vh; /* Ensure it takes full viewport height */
    padding: 1rem;
    /* background-color is inherited from :root in app.css */
  }

  .profile-container {
    text-align: center;
    padding: 2rem;
    background-color: rgba(45, 55, 72, 0.3); /* Slightly transparent card background #2d3748 with alpha */
    border-radius: 12px;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
  }

  .profile-pic {
    width: 150px;
    height: 100px;
    border-radius: 50%;
    margin-bottom: 1.5rem; /* Increased margin */
    /* background-color: #2d3748; /* Use button bg color */
    border: 3px solid #4a5568; /* Add a subtle border */
    display: inline-block;
    object-fit: cover; /* Ensure image covers the area */
  }

  h1 {
    margin-bottom: 0.5rem;
    font-size: 2.2em; /* Slightly adjusted size */
    color: #e2e8f0; /* Align with app.css */
    font-weight: 600; /* Slightly bolder */
  }

  .subtitle {
    font-size: 1.15em; /* Slightly larger */
    color: #a0aec0; /* Lighter gray for subtitle */
    margin-bottom: 2.5rem; /* Increased space before links */
    font-weight: 300;
  }

  .links-list {
    list-style: none;
    padding: 0;
    margin: 0;
    width: 100%;
    max-width: 350px; /* Adjusted max width */
  }

  .links-list li {
    margin-bottom: 1rem;
  }

  .link-button {
    display: block;
    padding: 0.9rem 1rem; /* Adjusted padding */
    background-color: #2d3748; /* Align with app.css button */
    color: #e2e8f0; /* Align with app.css */
    text-decoration: none;
    border-radius: 8px;
    transition: background-color 0.25s ease, transform 0.2s ease, box-shadow 0.2s ease; /* Added box-shadow transition */
    font-weight: 500;
    border: 1px solid transparent; /* Match button style */
  }

  .link-button:hover {
    background-color: #4a5568; /* Align with app.css button hover */
    transform: translateY(-3px); /* Slightly more lift */
    box-shadow: 0 6px 12px rgba(0, 0, 0, 0.3); /* Add shadow on hover */
    border-color: #63b3ed; /* Match button hover border */
  }

  /* Optional icon-specific styles can go here */
  /* Example:
  .link-button.twitter {
      background-color: #1DA1F2; // Twitter blue - consider if overriding theme is desired
  }
  .link-button.twitter:hover {
       background-color: #0c85d0;
  } */

</style>
