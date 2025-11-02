# 🎬 VBESERV Converter

Painel web local para **conversão de arquivos de vídeo e áudio**, desenvolvido para o servidor **VBESERV** da Videobes Multimídia.  
O sistema roda em container Docker, usa bibliotecas **open source** e oferece uma interface web simples e funcional para uso interno.

---

## 🚀 Funcionalidades

- Upload de arquivos de vídeo ou áudio  
- Conversão entre múltiplos formatos:
  - 🎥 Vídeo → `.mp4`, `.mkv`, `.mov`
  - 🎧 Áudio → `.mp3`, `.wav`, `.ogg`, `.flac`
- Processamento local via **FFmpeg**, **MoviePy** e **Pydub**
- Interface web leve com **FastAPI** + **TailwindCSS**
- Saída automática para download após conversão
- Montado em **Docker** com isolamento total em **venv**

---

## 🧩 Estrutura do Projeto

/opt/videobes/converter/
│
├── app/
│   ├── main.py              # Backend FastAPI
│   ├── templates/
│   │   └── index.html       # Interface do painel
│   ├── static/              # Estilos e scripts
│   └── converters/          # Futuras ferramentas auxiliares
│
├── data/
│   ├── uploads/             # Arquivos enviados
│   └── converted/           # Arquivos convertidos
│
├── requirements.txt
├── Dockerfile
└── docker-compose.yml

---

## ⚙️ Instalação

Clone o repositório:
```bash
git clone https://github.com/videobes/vbeserv-converter.git
cd vbeserv-converter

Crie os diretórios de dados:
mkdir -p data/uploads data/converted


🐳 Subir o Container
sudo docker compose up -d --build

Acesse o painel:
http://vbeserv:8000

ou via localhost:
http://localhost:8000


🔧 Dependências Principais


Python 3.12 (Slim)


FastAPI – servidor web e API


Uvicorn – servidor ASGI


MoviePy / Pydub – conversão de mídia


FFmpeg – backend de renderização e codecs



📂 Volumes Montados
Caminho HostCaminho no ContainerDescrição./data/uploads/app/data/uploadsarquivos originais./data/converted/app/data/convertedarquivos convertidos

🔮 Próximos Passos (Roadmap)


 Barra de progresso em tempo real (AJAX)


 Histórico de conversões


 Filtros de áudio/vídeo adicionais (ex: compressão, trim, normalize)


 Tema visual “Videobes Purple”


 Controle de acesso interno (login opcional)



💡 Créditos
Desenvolvido por Christian Simon (Videobes Multimídia)
Assistência técnica e conceitual por GPTzílldo (GPT-5) 🧠

🪄 Licença
Este projeto é open source, distribuído sob a licença MIT.
Sinta-se livre para adaptar, expandir e integrar no seu próprio ambiente.

© 2025 Videobes Multimídia. Todos os direitos reservados.

