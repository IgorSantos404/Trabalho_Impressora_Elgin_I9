📘 Sobre o Projeto
Este projeto foi desenvolvido como parte da disciplina de Algoritmos e Programação. O objetivo é criar uma aplicação Java capaz de se comunicar com a impressora térmica Elgin i8/i9 utilizando a biblioteca oficial da Elgin (E1_Impressora01.dll) e a ponte JNA (Java Native Access).
O programa simula um sistema de ponto de venda (PDV) simplificado, permitindo realizar login, configurar a conexão com a impressora, imprimir textos, QR Codes, códigos de barras, cupons fiscais (XML SAT), abrir a gaveta de dinheiro e emitir sinais sonoros. Todo o desenvolvimento foi realizado utilizando os conceitos de variáveis, estruturas condicionais (if/else), laços de repetição (for e while), vetores e métodos.
🧰 Tecnologias Utilizadas
•	Java (JDK 11 ou superior)
•	IntelliJ IDEA (IDE recomendada)
•	JNA (Java Native Access) - versão 5.15.0 (biblioteca jna-5.15.0.jar)
•	DLL da Elgin (E1_Impressora01.dll - versão 64 bits)
•	Git e GitHub para versionamento

📁 Estrutura do Projeto
text
/ (Raiz do projeto)
├── Main.java                  # Código-fonte principal (único arquivo editável)
├── E1_Impressora01.dll        # Biblioteca da impressora (64 bits)
├── libs Java/
│   └── jna-5.15.0.jar         # Ponte JNA para comunicação com a DLL
├── XMLSAT.xml                 # Arquivo de teste para impressão de cupom SAT
├── CANC_SAT.xml               # Arquivo de teste para cancelamento SAT
└── README.md                  # Documentação do projeto




⚙️ Como Executar o Projeto
🔽 1. Clonar ou baixar o projeto
1.	Acesse o repositório no GitHub.
2.	Faça o download do projeto (Download ZIP) ou clone via Git:
Bash

git clone https://github.com/seu-usuario/seu-repositorio.git


🧭 2. Importar no IntelliJ IDEA
1.	Abra o IntelliJ IDEA.
2.	Clique em File → Open e selecione a pasta do projeto.
3.	Se solicitado, clique em Trust Project.

📦 3. Configurar o JDK e a Biblioteca JNA
1.	Vá em File → Project Structure → Project.
2.	Em SDK, selecione um JDK 11 ou superior.
3.	Vá em Libraries, clique no botão + → Java.
4.	Selecione o arquivo libs Java/jna-5.15.0.jar e confirme.
5.	Os erros de com.sun.jna devem desaparecer.

🖨️ 4. Configurar a DLL e o Working Directory
1.	Certifique-se de que o arquivo E1_Impressora01.dll está na raiz do projeto (mesmo nível do Main.java).
2.	Vá em Run → Edit Configurations.
3.	Selecione a classe Main e verifique se o campo Working directory aponta para a pasta raiz do projeto.
4.	Ligue a impressora e conecte o cabo USB antes de executar.

▶️ 5. Executar
1.	Abra o arquivo Main.java.
2.	Clique no botão Run (▶️) ou pressione Shift + F10.
Nota sobre 32/64 bits: A DLL na raiz é de 64 bits. Se o seu Java for de 32 bits, substitua a DLL pela versão contida na pasta DLL 32 bits (x86). Verifique com java -version no terminal.




🔐 Login de Teste
O sistema possui autenticação com no máximo 3 tentativas. Utilize as credenciais abaixo:
•	Usuário: admin
•	Senha: 1234




 
Regra de Segurança: Todos os métodos de impressão verificam se a conexão está aberta antes de solicitar qualquer dado ao usuário. Se a conexão estiver fechada, o sistema exibe um aviso e retorna ao menu.
🧪 Testes Realizados
•	✅ Conexão via USB com a impressora Elgin i9.
•	✅ Impressão de texto simples com múltiplas cópias.
•	✅ Impressão de QR Code e Código de Barras.
•	✅ Leitura e impressão dos arquivos XMLSAT.xml e CANC_SAT.xml.
•	✅ Abertura da gaveta de dinheiro.
•	✅ Emissão de sinal sonoro e avanço de papel.
•	✅ Tratamento de erros (conexão fechada, retorno negativo da impressora, arquivo não encontrado).
👥 Autores
•	Flavia Etuany Gomes da Silva Cunha
•	Yuna Bellotto Vieira — RA: 077862
•	Leonardo Silva Gomes — RA: 248189
•	Igor Nogueira Alves dos Santos — RA: 246482

📚 Referências
•	Manual da Impressora Elgin i8/i9
•	Documentação do SDK Elgin — Elgin Developer Community
•	Documentação da biblioteca JNA (Java Native Access)
