<script>
	import '@fortawesome/fontawesome-free/css/all.css';
  
	let links = [
	  { title: "Shop", url: "https://example.com/home" },
	  { title: "Website", url: "https://example.com/blog" },
	  // ... add more personal links as needed
	];
  
	let socialLinks = [
	  { title: "Twitter", icon: "fab fa-twitter", url: "https://twitter.com/yourusername" },
	  { title: "Instagram", icon: "fab fa-instagram", url: "https://instagram.com/yourusername" },
	  { title: "LinkedIn", icon: "fab fa-linkedin-in", url: "https://linkedin.com/in/yourusername" },
	  // ... add more social links as needed
	];
  
	let profile = {
	  imageUrl: '/img/logo.png', // Replace with your image URL
	  description: 'This is a short bio or description about me or the page.'
	};
  </script>
  
  <style>
	body {
	  font-family: 'Arial', sans-serif;
	  background-color: #f4f4f4;
	  margin: 0;
	  padding: 0;
	  display: flex;
	  justify-content: center;
	  align-items: center;
	  height: 100vh;
	  text-align: center;
	}
  
	.link-container {
	  width: 100%;
	  max-width: 80%;
	  background-color: white;
	  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
	  border-radius: 15px;
	  padding: 20px;
	  margin: auto;
	  box-sizing: border-box;
	  text-align: center;
	}
  
	.profile-image {
	  width: 150px;
	  height: 150px;
	  border-radius: 50%;
	  margin: 0 auto 20px;
	  background-image: url('/img/logo.png');
	  background-size: cover;
	  background-position: center;
	}
  
	.description {
	  margin-bottom: 20px;
	  color: #333;
	  font-size: 16px;
	}
  
	.link-container a {
	  display: block;
	  background-color: #007bff;
	  color: white;
	  padding: 15px;
	  margin: 10px 0;
	  border-radius: 5px;
	  text-decoration: none;
	  transition: background-color 0.3s, transform 0.3s;
	}
  
	.link-container a:hover {
	  background-color: #0056b3;
	  transform: translateY(-2px);
	}
  
	.social-link {
	  display: flex;
	  align-items: center;
	  justify-content: center;
	}
  
	.social-link i {
	  margin-right: 8px;
	}
  
	@media (max-width: 600px) {
	  .link-container {
		width: 100%;
		max-width: 500px;
	  }
	}
  </style>
  
  <div class="link-container">
	<div class="profile-image"></div>
	<div class="description">{profile.description}</div>
  
	{#each links as link}
	  <a href="{link.url}" target="_blank">{link.title}</a>
	{/each}
  
	{#each socialLinks as link}
	  <a class="social-link" href="{link.url}" target="_blank">
		<i class="{link.icon}"></i>
		{link.title}
	  </a>
	{/each}
  </div>
  