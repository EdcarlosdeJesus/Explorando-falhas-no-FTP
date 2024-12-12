# Explorando-falhas-no-FTP
➡️Sobre Metasploit

![image](https://github.com/user-attachments/assets/15fdd8a8-0f32-4c6e-95af-83c374987382)


---

➡️ Iniciaremos abrindo nossa ferramenta de pesquisa e ataque.
 
![image](https://github.com/user-attachments/assets/e3f5eaec-5f6e-4bf6-902b-585e26da2ac1)

--- 

➡️ No kali iniciaremos com o comando msfcosole para iniciar o console como mostra a imagem abaixo.

![image](https://github.com/user-attachments/assets/67778307-9344-415e-bdd4-7f1d0455e311)

---

➡️ Procurando por **vsftpd** um exploit malicioso que explora um backdoor foi encontrado em 2011.

 
 ![image](https://github.com/user-attachments/assets/42dedc7c-c198-494b-9f0c-1227479f32fd)

➡️ Desejando saber sobre essa vulnerabilidade basta executar esse caminho:

 <info exploit/unix/ftp/vsftpd_234_backdoor>
 
![image](https://github.com/user-attachments/assets/bd0ea8eb-09eb-42ad-90a5-86056baea61f)

➡️ Para usar muito simples apenas colocando o comando ***use***

comando:***use exploit/unix/ftp/vsftpd_234_backdoor***

 
****
-Comando ***show options*** mostra sobre o nosso módulo, e já temos nossa porta mas precisamos do nosso IP de destino.

![image](https://github.com/user-attachments/assets/34467a44-e623-4ae6-a9f2-51e95557bba2)

****
➡️Na maquina de destino que seria nosso metasploitable usaremos o comando *IP addr* assim consiguiremos ver nosso ip alvo.

➡️Configuração para nosso host remoto ***set rhost***.

![image](https://github.com/user-attachments/assets/cdf093c1-b79c-462c-85ad-a4af5654a4f3)

****
➡️Comando ***show payloads*** mostrará os módulos.

![image](https://github.com/user-attachments/assets/ff60068c-1d17-4218-ba9c-dd5ac855834f)

➡️ *Interact* esse payload comando em unix ele interage com uma conexão estabelecida, consigo de forma remota accesar outro computador de forma remota explorando backdoor.

➡️ Comando *set payload payload/cmd/unix/interact* usado para definir o payload (carga útil) que será usado em conjunto com o exploit.

➡️ payload *cmd/unix/interact* permite a interação com uma conexão de shell estabelecida. Isso significa que, após explorar a vulnerabilidade e obter uma sessão de shell no sistema alvo, podemos usar esse payload para executar comandos diretamente na shell do sistema comprometido.

![image](https://github.com/user-attachments/assets/c7c76c96-1226-4b70-aeb6-8a04ec83dca9)


****
➡️ Confirmado no nosso Host Alvo, iremos da inicio ao nosso exploit pelo comando *exploit*

![image](https://github.com/user-attachments/assets/e6c1c942-fe43-48b5-a0e3-e3b7888748f9)

****
➡️ Depois de uma conexão estabelecida com o comando *ls* veremos oque temos na máquina alvo.

![image](https://github.com/user-attachments/assets/35e6165b-e3f4-447e-8c83-c41c04c83ef7)

****

➡️ Observamos que estamos com ip da máquina remota

![image](https://github.com/user-attachments/assets/0dd5ef34-5ed6-44d4-8527-02a973efa8eb)

****
-Semelhante a CTF no inicio desse lab criei um arquivo como *flag.txt* dessa forma saberia que conseguir invadir a máquina alvo, abaixo imagem comprovando o sucesso desse lab.

![image](https://github.com/user-attachments/assets/0c396210-38d9-4c29-b776-2d0c3b507d62)

➡️ Desejando abrir o arquivo apenas usar o comando nano flag.txt





















