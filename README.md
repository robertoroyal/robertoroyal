<h2 align="left" class="text-3xl font-bold text-blue-600">Olá! 👋 Como você está? Seja muito bem-vindo ao meu perfil! Fico feliz em tê-lo aqui!</h2>  

<p align="left" class="mt-4 text-lg">Meu nome é <strong>Roberto Silva</strong>, sou estudante de programação e desenvolvimento web.</p>  

<img align="left" height="200" src="https://github.com/robertoroyal/Foto/blob/main/Treino%20boxe/Imagem%20do%20WhatsApp%20de%202024-08-25%20%C3%A0(s)%2018.31.38_dd432447.jpg" class="rounded-full border-2 border-blue-500" />    

<p align="left" class="mt-4 text-lg">✨ Creating bugs since 2024<br>📚 Desenvolvedor com experiência em lojas Magento, atualmente aprimorando minhas habilidades na plataforma.<br>🎯 Goals: Mãos à obra.<br>🎲 Fun fact: Tecnologia e Inovação.</p>   

<h3 align="left" class="mt-6 text-2xl font-semibold">I code with:</h3>   
<div align="left" class="flex space-x-2 mt-2">  
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" height="40" alt="html5 logo" />  
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" height="40" alt="css3 logo" />   
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" height="40" alt="javascript logo" />  
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" height="40" alt="python logo" />  
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" height="40" alt="react logo" />  
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nextjs/nextjs-original.svg" height="40" alt="nextjs logo" />  
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg" height="40" alt="nodejs logo" />  
</div>  

<h3 align="left" class="mt-6 text-2xl font-semibold">Notícias em tempo real:</h3>   
<div id="news" class="flex flex-col space-y-4"></div>  

<h3 align="left" class="mt-6 text-2xl font-semibold">Conecte-se comigo:</h3>  
<div align="left" class="flex space-x-4 mt-2">   
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

<script>
// Substitua com sua chave de API
const API_KEY = '040912216cdf4ba489567dd8324a8d71';
const url = `https://newsapi.org/v2/top-headlines?category=technology&language=pt&apiKey=${API_KEY}`;

fetch(url)
  .then(response => response.json())
  .then(data => {
    const newsContainer = document.getElementById('news');
    data.articles.forEach(article => {
      const newsItem = document.createElement('div');
      newsItem.innerHTML = `
        <h4 class="text-xl font-bold">${article.title}</h4>
        <p>${article.description}</p>
        <a href="${article.url}" target="_blank">Leia mais</a>
      `;
      newsContainer.appendChild(newsItem);
    });
  })
  .catch(error => {
    console.error('Erro ao carregar notícias:', error);
  });
</script>
