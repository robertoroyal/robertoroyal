<h2 class="text-3xl font-bold text-blue-600">Olá! 👋 Como você está? Seja muito bem-vindo ao meu perfil! Fico feliz em tê-lo aqui!</h2>  

<p class="mt-4 text-lg">Meu nome é <strong>Roberto Silva</strong>, sou estudante de programação e desenvolvimento web.</p>  

<img   
  height="200"   
  src="https://github.com/robertoroyal/Foto/blob/main/Treino%20boxe/Imagem%20do%20WhatsApp%20de%202024-08-25%20%C3%A0(s)%2018.31.38_dd432447.jpg"   
  class="rounded-full border-2 border-blue-500"   <p class="mt-4 text-lg">✨ Creating bugs since 2024<br>📚 Desenvolvedor com experiência em lojas Magento, atualmente aprimorando minhas habilidades na plataforma.<br>🎯 Goals: Mãos à obra.<br>🎲 Fun fact: Tecnologia e Inovação.</p>  
/>  



<h3 class="mt-6 text-2xl font-semibold">Repositórios Populares do GitHub:</h3>  
<ul id="trending-repos" class="list-disc pl-5 text-lg">Carregando repositórios...</ul>  

<h3 class="mt-6 text-2xl font-semibold">Últimas Notícias de Tecnologia:</h3>  
<ul id="tech-news" class="list-disc pl-5 text-lg">Carregando notícias...</ul>  

<script>  
  async function fetchTrendingRepos() {  
    try {  
      const response = await fetch('https://api.github.com/search/repositories?q=created:>2023-01-01&sort=stars&order=desc');  
      if (!response.ok) throw new Error('Falha ao buscar repositórios.');  

      const data = await response.json();  
      const repos = data.items.slice(0, 5);  
      const repoList = repos.map(repo => `  
        <li>  
          <a href="${repo.html_url}" target="_blank">${repo.name}</a> - ${repo.stargazers_count} estrelas  
        </li>  
      `).join('');  

      document.getElementById('trending-repos').innerHTML = repoList;  
    } catch (error) {  
      console.error('Erro ao buscar repositórios populares:', error);  
      document.getElementById('trending-repos').innerText = 'Erro ao carregar repositórios';  
    }  
  }  

  async function fetchTechNews(apiKey) {  
    try {  
      const response = await fetch(`https://newsapi.org/v2/everything?q=technology&sortBy=publishedAt&apiKey=${apiKey}`);  
      if (!response.ok) throw new Error('Falha ao buscar notícias.');  

      const data = await response.json();  
      const articles = data.articles.slice(0, 5);  
      const newsList = articles.map(article => `  
        <li>  
          <a href="${article.url}" target="_blank">${article.title}</a> - ${new Date(article.publishedAt).toLocaleString()}  
        </li>  
      `).join('');  

      document.getElementById('tech-news').innerHTML = newsList;  
    } catch (error) {  
      console.error('Erro ao buscar notícias de tecnologia:', error);  
      document.getElementById('tech-news').innerText = 'Erro ao carregar notícias.';  
    }  
  }  

  const apiKey ='a44dd0536a28417fba8c492b9a2a773d'; // Substitua pela sua chave da API de forma segura  
  fetchTrendingRepos();  
  fetchTechNews(apiKey);  
</script>  

<h3 class="mt-6 text-2xl font-semibold">Conecte-se comigo:</h3>  
<div class="flex space-x-4 mt-2">   
  <a href="https://www.instagram.com/robertto_royal/" target="_blank">  
    <img src="https://raw.githubusercontent.com/maurodesouza/profile-readme-generator/master/src/assets/icons/social/instagram/default.svg" width="52" height="40" alt="instagram logo" />  
  </a>  
  <a href="https://www.facebook.com/joseroberto.dasilva/" target="_blank">  
    <img src="https://raw.githubusercontent.com/maurodesouza/profile-readme-generator/master/src/assets/icons/social/facebook/default.svg" width="52" height="40" alt="facebook logo" />  
  </a>  
  <a href="https://www.youtube.com/@RRobertoRoyal" target="_blank">  
    <img src="https://raw.githubusercontent.com/maurodesouza/profile-readme-generator/master/src/assets/icons/social/youtube/default.svg" width="52" height="40" alt="youtube logo" />  
  </a>  
  <a href="https://www.linkedin.com/in/joserobertodasilva917610022/" target="_blank">  
    <img src="https://raw.githubusercontent.com/maurodesouza/profile-readme-generator/master/src/assets/icons/social/linkedin/default.svg" width="52" height="40" alt="linkedin logo" />  
  </a>  
  <a href="https://web.telegram.org/a/" target="_blank">  
    <img src="https://raw.githubusercontent.com/maurodesouza/profile-readme-generator/master/src/assets/icons/social/telegram/default.svg" width="52" height="40" alt="telegram logo" />  
  </a>  
</div>
