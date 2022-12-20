# custom-kernel-5.16.0-rc1-apl

1. Se o sistema tiver recém-formatado, dê um apt update e depois um upgrade pra deixar tudo atualizado e evitar erros.
2. Instale o .deb da pasta raiz (firmware-sof-signed_1.7-1_all.deb)
3. Após isso, extraia o arquivo kernel.zip, e dentro da pasta kernel instale cada um dos .deb lá:
```sh
sudo dpkg -i *.deb
```
4. Volte, e agora vá na pasta tplg e copie todos os arquivos de lá para a pasta raiz custom-kernel-5.16.0-rc1-apl
5. Entre como administrador com o sudo su, dê permissão para executar no arquivo make.sh com o chmod +x , e então execute-o ./make.sh:
```sh
sudo su
chmod +x make.sh
./make.sh
```
6. Após o processo ter terminado, reinicie o seu PC, selecione o novo kernel (5.16.0-rc1-apl) e provavelmente o áudio estará funcionando.

Eu testei esse processo na distro Lubuntu 22.04.1 LTS x86_64 e funcionou muito bem, mas obtive esse tutorial com um usuário da comunidade Diolinux Plus, que testou com o Ubuntu e Linux Mint, segue o link: https://plus.diolinux.com.br/t/notebook-positivo-n1250-sem-som-no-linux/42628/2

Esse projeto foi baseado originalmente no projeto https://github.com/yangxiaohua2009/custom-kernel
