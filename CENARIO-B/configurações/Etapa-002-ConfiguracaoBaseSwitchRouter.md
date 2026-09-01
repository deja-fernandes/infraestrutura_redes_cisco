COMANDOS PARA CONFIGURAÇÃO DO SWITCH CISCO CATALYST LAYER 2 2960 (SW-B-001)

Acessando o modo Exec Privilegiado: enable

Configuração de Data/Hora em inglês (Abreviado ou Completo): clock set 14:00:00 1 Sep 2026

Acessando o modo de configuração global de comandos:

    Configuração do nome do switch: hostname SW-B-001

    Habilitando o serviço de criptografia de senhas do Tipo-7 Password (criptografia defasada): service password encryption

    Habilitando o serviço de marcação de Data/Hora detalhado nos Logs: service timestamp log datetime msec

    Habilitando o tamanho do buffer dos logs na memória RAM: loggin buffered 4096

    Desativando a resolução de nomes de domínio: no ip domain-lookup

    Configuração do banner da mensagem do dia: banner mtod "mensagem"

    Habilitando o uso de senha do Tipo-5 secret para acessar o modo EXEC Privilegiado: enable secret senha

    Criação dos usuários locais utilizando senhas do Tipo-5 e privilégios diferenciados: 
        username seu_usuário_1 secret sua_senha_1
        username seu_usuário_2 secret sua_senha_2
        username seu_usuário_3 privilege 15 secret seua_senha_3

    Configuração do nome de domínio FQDN (Nome de domínio totalmente qualificado): ip domain-name seu_dominio.br

    Criação da chave de criptografia e habilitar o serviço de SSH Server local: crypto key generate rsa general-keys modulus 1024

    Habilitando a versão 2 do serviço de SSH Server: ip ssh authentication-retries 2

    Desativando os serviços de descobertas de equipamentos na rede: no cdp run // no lldp run

    Acessando a linha console, porta padrão de acesso out-of-band: line console 0

        Forçando fazer login local utilizando usuário e senhas locais do switch: login local

        Habilitando senha de acesso do Tipo-7 Password: password sua_senha_não_segura

        Sincronizando as mensagens de logs na tela: loggin synchronous

        Saindo de todos os níveis e voltando para o modo EXEC Privilegiado
    
    Acessando as linhas virtuais de acesso remoto do Switch: line vty 0 4

        Forçando fazer login local utilizando usuário e senha locais do switch: login local

        Habilitando senha de acesso do Tipo-7 password: password sua_senha_não_segura

        Sincronizando as mensagens de logs na tela: logging synchronous

        Habilitando o tempo de inatividade de uso da linha virtual: exec-timeout 5 30

        Configuração do tipo de protocolo de transporte de entrada: transport input ssh

        Saindo de todos os níveis e voltando para o modo EXEC Privilegiado:

    Salvando as configurção da memória RAM para a memória NVRAM: copy running config startup config

    Mostrando as configurações atuais feitas no switch sem salvar: show runnning config

    Mostrando as configurações salvas no switch: show startup config

