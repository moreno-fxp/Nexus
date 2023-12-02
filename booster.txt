(function() {
    const html = `
    <div id="Open">
      <h1 id="Openh1">OpenSource</h1>
      <button id="OpenSourceInject">OpenSource</button>
      <div id="TextGPT">
      <div id="TextImgCredits">|</div>
      <div id="TextImgCredits2">NEXUS</div>
      </div>
      <a href="https://discord.gg/mZddPyTJ" target="_blank">   
      <img id="ImgCredits" src="https://i.pinimg.com/736x/8d/8f/40/8d8f4089b49c9101b9e39b793f7279fa.jpg" alt="Bypass">
    </a>
      </div>
      <div id="OpenExecutado" style="display: none;">
          <p id="animatedText">Script Injetado. Inicie uma nova conversa</p>
      </div>
    `;
    
    const css = `
  
    .open-bg-purple{
    background-color: rgba(171, 2, 255, 0.281);
    }
     
    .open-border-purple{
      border-color: rgb(171, 104, 255);
    }
  
    .open-text-purple {
      color: rgb(171, 104, 255); 
  }
  
    #ByPassButton{
      background-color: rgb(171, 104, 255); 
          color: white;
          padding: 10px 20px;
          border: none;
          border-radius: 5px;
          cursor: pointer;
          font-size: 18px;
          border-radius: 8px;
          height: auto;
          width: 20%;
          box-shadow: 0 0 5px rgb(171, 104, 255);
  }
  
    #TextGPT{
      position: absolute;
      top: 20px;
      left: 105px;
      overflow: hidden;
      height: 150px;
      width: 300px;
  }
  
  #TextImgCredits2 {
    position: absolute;
      font-size: 50px;
      color: rgb(171, 104, 255);
      left: 100px;
      transform: translateX(-230%);
      transition: transform 1s;
      top: 5px;
      color: rgb(171, 104, 255);
      text-shadow: 0 0 10px rgb(171, 104, 255);
  }
  
  #TextImgCredits:hover + #TextImgCredits2 {
      transform: translateX(-50%);
  }
  
  #TextImgCredits {
  position: absolute;
  color: rgb(171, 104, 255);
  position: absolute;
  font-size: 50px;
  left: 0px;
  cursor: pointer;
  color: rgb(171, 104, 255);
  text-shadow: 0 0 10px rgb(171, 104, 255);
  transform: scaleX(1.5); 
  }
  
  #ImgCredits {
  border: 2px solid black;
  border-radius: 20px;
  cursor: pointer;
  transition: box-shadow 0.7s, transform 0.7s;
  width: 80px;
  height: 80px;
  position: absolute;
  top: 15px; 
  left: 15px;
  background-color: rgba(255, 255, 255, 0.2); 
  }
  
  #ImgCredits:hover {
  box-shadow: 0 0 7px 5px rgb(171, 104, 255);
  filter: blur(0.5px);
  transform: scale(1.1);
  }
  
  #animatedText {
  animation-name: scaleIn;
  animation-duration: 1.5s;
  animation-delay: 0.5s;
  animation-fill-mode: both;
  transform-origin: center;
  }
  
  @keyframes scaleIn {
  from {
    opacity: 0;
    transform: scale(0.1);
  }
  to {
    opacity: 1;
    transform: scale(2);
  }
  }
  
  @keyframes scalePrompt {
  from {
  opacity: 0;
  transform: scale(0.1);
  }
  to {
  opacity: 1;
  transform: scale(1.0);
  }
  }
  
  
    #OpenExecutado {
    width: 300px;
    height: 200px;
    position: absolute;
    top: 50%;
    left: 50%;
    text-shadow: 0 0 10px rgb(171, 104, 255);
    transform: translate(-50%, -50%);
    text-align: center;
    background-color: transparent;
    padding: 20px;
    display: none;
    color: rgb(171, 104, 255);
    transition: 0.5s;
  }
  
  #Openh1, #OpenSourceInject {
  margin: 20px 0;
  }
  
     #Openh1 {
      margin-top: 110px;
      font-size: 36px;
      color: rgb(171, 104, 255);
      text-shadow: 0 0 10px rgb(171, 104, 255);
  }
  
  #OpenSourceInject {
      background-color: rgb(171, 104, 255); 
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      font-size: 18px;
      border-radius: 8px;
      width: 70%;
      transition: 0.5s;
      box-shadow: 0 0 5px rgb(171, 104, 255);
  }
  
  #Open {
    overflow: hidden;
    width: 300px;
    height: 400px;
    position: absolute;
    top: 25%;
    left: 45%;
    transform: translate(-50%, -50%);
    text-align: center;
    background-color: #343541;
    border: 3px solid transparent;
    border-image: linear-gradient(90deg, rgb(171, 104, 255), rgb(25, 195, 125));
    border-image-slice: 1;
    border-radius: 10px;
    animation-name: scalePrompt;
    animation-duration: 1.5s;
    animation-delay: 0.5s;
    animation-fill-mode: both;
  }
  
  #OpenSourceInject:hover {
      transform: scale(1.1);
  }
  
    `;
  
    const js = `
    const texto = "Seu texto da OpenSource aqui"; /* Coloque o texto da Opensource aqui dentro */
  
  
    document.getElementById("OpenSourceInject").addEventListener('click', OpenClick);
    function OpenClick(){
  
      function executeCode() {
        const TextoCompleto = document.querySelectorAll('.text-orange-500:not(.processed)');
    
        for (let i = 0; i < TextoCompleto.length; i++) {
            const resposta = TextoCompleto[i];
            resposta.classList.remove("text-orange-500");
            resposta.classList.add("text-white-500");
            resposta.classList.add("processed");
        }
  
        const EnvButton = document.querySelector('[class="absolute p-1 rounded-md md:bottom-3 md:p-2 md:right-3 dark:hover:bg-gray-900 dark:disabled:hover:bg-transparent right-2 gizmo:dark:disabled:bg-white gizmo:disabled:bg-black gizmo:disabled:opacity-10 disabled:text-gray-400 enabled:bg-brand-purple gizmo:enabled:bg-black text-white gizmo:p-0.5 gizmo:border gizmo:border-black gizmo:rounded-lg gizmo:dark:border-white gizmo:dark:bg-white bottom-1.5 transition-colors disabled:opacity-40"]');
        if(EnvButton){
        EnvButton.className = "absolute p-1 rounded-md md:bottom-3 md:p-2 md:right-3 dark:hover:bg-gray-900 dark:disabled:hover:bg-transparent right-2 gizmo:dark:disabled:bg-white gizmo:disabled:opacity-10 disabled:text-gray-400 enabled:bg-brand-purple text-white gizmo:p-0.5 gizmo:border gizmo:rounded-lg bottom-1.5 transition-colors disabled:opacity-40";
        }
  
        const envSVG = document.querySelector('svg[class="text-white dark:text-black"]');
        if (envSVG) {
        envSVG.classList.remove('dark:text-black');
        envSVG.classList.add('dark:text-white');
        }
  
        const h1Element = document.querySelector('h1.text-4xl');
  
      if (h1Element) {
        h1Element.textContent = "OpenSource";
      }
  
  const textArea = document.getElementById("prompt-textarea");
  let messageAlreadyAdded = false;
  
  if (textArea) {
  textArea.setAttribute("placeholder", "OpenSource 💜");
  
  textArea.addEventListener('keydown', function (event) {
    if (event.keyCode === 13 && !event.shiftKey) {
      event.preventDefault();
  
      if (!messageAlreadyAdded) {
        if (!textArea.value.includes(texto)) {
          textArea.value = texto + textArea.value;
        }
        
        messageAlreadyAdded = true; 
      }
    }
  });
  }
  
        const OpenSource = document.querySelector('[class="mb-5 text-2xl font-medium"]');
        if(OpenSource){
          OpenSource.textContent = 'OpenSource';
        }
  
        const Nomechat = document.querySelector('[class="group flex cursor-pointer items-center gap-1 rounded-xl py-2 px-3 text-lg font-medium hover:bg-gray-50 radix-state-open:bg-gray-50 dark:hover:bg-black/10 dark:radix-state-open:bg-black/20"] > div');
        if(Nomechat){
            Nomechat.innerHTML = 'OpenSource <span class="text-token-text-secondary">3.5</span>'
        }
  
        const divImage = document.querySelector('[class="relative flex h-full max-w-full flex-1 flex-col overflow-hidden"]');
        if(divImage){    
        const urlImg = 'https://i.pinimg.com/736x/8d/8f/40/8d8f4089b49c9101b9e39b793f7279fa.jpg';
        divImage.style.backgroundImage = 'url(' + urlImg + ')';
        divImage.style.backgroundSize = 'cover';
        divImage.style.backgroundPosition = 'center';
        }
        
        const CircleSvg = document.querySelectorAll('[class="gizmo-shadow-stroke relative flex h-full items-center justify-center rounded-full bg-white text-black"]');
        if (CircleSvg) {
        for (let i = 0; i < CircleSvg.length; i++) {
        const resposta = CircleSvg[i];
  
        resposta.style.backgroundColor = 'rgb(171, 104, 255)';
  
        resposta.classList.remove('text-black', 'bg-white');
  
        resposta.classList.add('text-white', 'bg-white');
        }
    }
  
  
        const txtc = document.querySelectorAll('[class="min-h-[20px] text-message flex flex-col items-start gap-3 whitespace-pre-wrap break-words [.text-message+&]:mt-5 overflow-x-auto"]');
  for (let i = 0; i < txtc.length; i++) {
    const resposta = txtc[i];
    const textContent = resposta.textContent;
    if (textContent.startsWith(texto)) {
      const newText = textContent.replace(texto, '');
      resposta.textContent = newText;
    }
  }
  
        const Gpt35Cor = document.querySelector('[class="icon-sm transition-colors text-brand-green"]');
  if(Gpt35Cor) {
    Gpt35Cor.classList.remove('text-brand-green');
    Gpt35Cor.classList.add('open-text-purple');
  }
  
  const Gpt35Texto = document.querySelectorAll('[class="truncate text-sm font-medium md:pr-1.5 pr-1.5"]');
  if(Gpt35Texto){
    for (let i = 0; i < Gpt35Texto.length; i++) {
      const resposta = Gpt35Texto[i];
      if(resposta.textContent === 'GPT-3.5'){
        resposta.textContent = 'OpenSource 3.5'
      } 
      if(resposta.textContent === 'GPT-4'){
        resposta.textContent = 'OpenSource 4'
      }
        
  }
  }
  
        const ftChatGpt = document.querySelectorAll('[class="relative p-1 rounded-sm h-9 w-9 text-white flex items-center justify-center"]');
  if(ftChatGpt){
      for (let i = 0; i < ftChatGpt.length; i++) {
          const resposta = ftChatGpt[i];
          resposta.style = 'background-color: rgb(171, 104, 255); width: 36px; height: 36px;';
      }
  }
  
  const NomeResposta = document.querySelectorAll('[class="font-semibold select-none"]');
  if(NomeResposta){
    for (let i = 0; i < NomeResposta.length; i++) {
        const resposta = NomeResposta[i];
        const nome = resposta.textContent;
        if( nome === "ChatGPT"){
            resposta.textContent = 'OpenSource'
        }
  
    }
  }
    
        const CordoErro = document.querySelectorAll('[class="mb-2 py-2 px-3 border text-gray-600 rounded-md text-sm dark:text-gray-100 border-orange-500 bg-orange-500/10"]');
    
        for (let i = 0; i < CordoErro.length; i++) {
            const resposta = CordoErro[i];
            const classesARemover = ['py-2', 'px-3', 'border', 'text-gray-600', 'rounded-md', 'text-sm', 'dark:text-gray-100', 'border-orange-500', 'bg-orange-500/10'];
            classesARemover.forEach(function (classe) {
                resposta.classList.remove(classe);
            });
            resposta.classList.add('py-2', 'px-3', 'border', 'open-text-purple', 'rounded-md', 'text-sm', 'dark:text-white-100', 'open-border-purple', 'open-bg-purple');
            resposta.textContent = 'Erro removido pelo Bypass 💜🤖';
            resposta.classList.add('processed');
        }
    
        const ftErro = document.querySelectorAll('[class="absolute w-4 h-4 rounded-full text-[10px] flex justify-center items-center right-0 top-[20px] -mr-2 border border-white bg-orange-500 text-white"]:not(.processed)');
    
        for (let i = 0; i < ftErro.length; i++) {
            const resposta = ftErro[i];
            resposta.remove();
        }
    
    }
    
    setInterval(executeCode, 0);
  
  
        document.getElementById("Open").style.display = "none";
    setTimeout(function() {
        const openExecutado = document.getElementById("OpenExecutado");
        openExecutado.style.display = "block";
  
        openExecutado.style.opacity = 1;
        setTimeout(function(){
            openExecutado.style.opacity = 0;
        }, 3000);
    }, 2000);
  const originalFetch = window.fetch;
  window.fetch = function (url, options) {
  if (url.includes('chat.openai.com/v1/moderations') || url.includes('api.openai.com/v1/moderations')) {
    return new Promise(() => {});
  } else {
    return originalFetch(url, options).then((response) => {
      return response;
    });
  }
  }
  };
    `;
  
    var style = document.createElement('style');
        style.textContent = css;
      
        var container = document.createElement('div');
        container.innerHTML = html;
      
        const head = document.head;
        const body = document.body;
        var script = document.createElement('script');
        script.textContent = js;
    
        head.appendChild(style);
        body.appendChild(container);
        body.appendChild(script);
    })();
