📹 MediaMTX com Transcodificação de Câmeras RTSP
Olá, nesse arquivo vamos esclarecer o processor de cofiguração e uso de uma parte essencial do nosso projeto. Este projeto utiliza o MediaMTX (antigo rtsp-simple-server) para gerenciar e servir múltiplas câmeras RTSP. Algumas câmeras funcionam diretamente, enquanto outras precisam passar por uma etapa de transcodificação com FFmpeg para serem acessíveis de forma estável.

🔧 Pré-requisitos
1. MediaMTX
Faça o download da versão mais recente do MediaMTX para seu sistema operacional a partir do repositório oficial, ou use a versão já disponibilizada pela gente nesse repositório.

📦 https://github.com/bluenviron/mediamtx/releases

Após o download, descompacte e execute:
./mediamtx

2. FFmpeg (Obrigatório para transcodificação)
FFmpeg é necessário para transcodificar algumas streams de câmera. Baixe e instale conforme seu sistema:

🔗 https://ffmpeg.org/download.html

Após baixar o ffmpeg, será necessário rodar o exe dentro da pasta bin, chamado ffmpeg.exe.
Com isso concluído, basta colocar o path do ffmpeg nas variáveis de ambiente do sistema.

✏️ Alterações no Código

O código "mediamtx.yml" não vem modificado, mas o disponível nesse repositório já apresenta as moficações necessárias para rodar o sistema.
Ele conta com:

-> Inclusão de múltiplas câmeras com endereços RTSP.

-> Uso de runOnInit com FFmpeg para transcodificar streams que não funcionam corretamente de forma direta.

-> Configuração de reinicialização automática com runOnInitRestart: yes

▶️ Execução

Após configurar o arquivo mediamtx.yml, basta iniciar o MediaMTX manualmente ou pelo terminal do visual studio com o comando:

./mediamtx

📞 Suporte
Para dúvidas ou melhorias, consulte a documentação oficial ou abra uma issue neste repositório.
