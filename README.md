# 💻 Pos-install do Arch Linux.

<p align = "center">
    <img src="https://github.com/DarlysonGabriel/archlinux-pos-install/blob/main/Imgs/Arch%20Linux%20logo/ca1e3cbffbdb38fad2f932b9b83827a8.jpg" alt="Logo" width="100">
</p>
Sabemos que, nos dias de hoje, o Linux (de forma geral) vem sendo uma alternativa boa oara usuários de Windows.

Para intusiastas da tecnologia (como programadores) um nom sistema que agrade e, ao mesmo tempo, seja útil e eficaz, acaba sendo um recurso essencial para aesse publico.


O Arch Linux é uma boa solução a o sistema da Microsoft, trazendo controle total e personalização extrema.

Mas, para o encarar, você deve entender algumas coisas sobre este sistema.

## Detalhes antes da instalação

Antes de instalar o Arch Linux, é importante entender alguns pontos sobre a distribuição.

### 1. Não existe uma instalação "definitiva"

Não há uma única forma correta de instalar ou utilizar o Arch Linux. Ele é uma distribuição altamente personalizável, permitindo que cada usuário monte seu sistema de acordo com suas necessidades.

Você pode utilizá-lo para:
- 💻 Uso doméstico
- 👨‍💻 Desenvolvimento de software
- 🎮 Jogos
- 🖥️ Computadores antigos
- ⚡ Sistemas minimalistas
- 🖧 Servidores
- 🔒 Segurança e estudos

Cada instalação pode possuir pacotes, serviços e interfaces gráficas completamente diferentes.

---

### 2. O Arch Linux não possui uma interface gráfica oficial

Após a instalação, o Arch Linux inicia apenas em modo terminal. Caso deseje uma interface gráfica, será necessário instalar uma por conta própria.

Abaixo estão algumas das interfaces gráficas e gerenciadores de janelas mais populares.

| Interface | Popularidade | Indicação de uso |
|-----------|--------------|------------------|
| **GNOME** | Muito popular entre empresas, desenvolvedores e usuários do Ubuntu/Fedora | Interface moderna, limpa e focada em produtividade. |
| **KDE Plasma** | Muito popular entre usuários vindos do Windows | Interface altamente personalizável, moderna e rica em recursos. |
| **XFCE** | Muito utilizada em computadores antigos | Interface leve, simples e extremamente estável. |
| **Cinnamon** | Muito popular entre usuários do Linux Mint | Interface tradicional semelhante ao Windows. |
| **MATE** | Popular entre usuários que preferem o GNOME clássico | Interface leve, tradicional e estável. |
| **LXQt** | Muito utilizada em computadores com poucos recursos | Interface extremamente leve e rápida. |
| **LXDE** | Popular em computadores muito antigos | Interface simples e com consumo mínimo de recursos. |
| **Budgie** | Popular entre usuários que buscam um visual moderno | Interface elegante e fácil de utilizar. |
| **Deepin Desktop (DDE)** | Popular entre usuários que gostam de um visual refinado | Interface bonita, inspirada no macOS e intuitiva. |
| **Hyprland** | Muito popular entre entusiastas do Wayland | Compositor moderno, com animações e alta personalização. |
| **Sway** | Popular entre usuários avançados | Compositor Wayland baseado no i3, focado em produtividade. |
| **i3** | Muito utilizado por programadores | Gerenciador de janelas em mosaico controlado por teclado. |
| **Openbox** | Popular entre usuários minimalistas | Gerenciador de janelas extremamente leve e configurável. |
| **IceWM** | Utilizado em computadores muito antigos | Interface clássica e de baixíssimo consumo. |
| **Enlightenment** | Popular entre quem busca leveza com efeitos visuais | Interface rápida, bonita e altamente personalizável. |

> **💡 Dica:** Caso seja seu primeiro contato com o Arch Linux, recomenda-se utilizar **GNOME**, **KDE Plasma**, **XFCE** ou **Cinnamon**, pois oferecem uma experiência mais amigável para iniciantes, além se serem relativamente leve.

### 3. A instalação: o Arch Lumix não é como outras distribuições

Diferente da maioria das distribuições Linux, o **Arch Lumix** não possui um instalador gráfico tradicional. Em vez disso, a instalação é realizada principalmente pelo terminal, permitindo que o usuário tenha controle total sobre o sistema.

<p align="center">
  <img src="https://www.edivaldobrito.com.br/wp-content/uploads/2023/12/arch-linux-2023-12-01-lancado-com-o-archinstall-2-7-e-kernel-6-6-1024x585.webp" width="700">
  <br>
  <em>Tela do instalador Arch Linux.</em>
</p>

Durante o processo, você escolherá quais componentes serão instalados, como:
- Kernel do Linux;
- Ambiente gráfico (caso deseje);
- Gerenciador de inicialização (Bootloader);
- Drivers de vídeo;
- Serviços do sistema;
- Programas essenciais.

Isso faz com que cada instalação seja única, contendo apenas o que o usuário realmente precisa.

> **💡 Dica:** Embora possa parecer mais difícil no início, esse método resulta em um sistema mais leve, organizado e totalmente personalizado para o seu uso.


# Como instalar o Arch Linux?

Para instalar o Arch Linux, temos várias formas. Uma delas é pelo `archinstall`

# Instalando o Arch Linux com o `archinstall`

O **archinstall** é o instalador oficial do Arch Linux. Ele oferece uma instalação guiada pelo terminal, tornando o processo muito mais simples do que a instalação totalmente manual.

> **⚠️ Atenção:** A instalação apagará os dados do disco selecionado. Faça um backup antes de continuar.

---

# 1. Inicie pelo pendrive

Inicialize o computador utilizando o pendrive do Arch Linux.

Quando o sistema terminar de carregar, você verá um terminal semelhante a este:

```bash
root@archiso ~ #
```

---

# 2. Conecte-se à internet

### Via cabo (Ethernet)

Na maioria dos casos, a conexão é automática.

Verifique com:

```bash
ping archlinux.org
```

---

### Via Wi-Fi

Execute:

```bash
iwctl
```

Dentro do `iwctl`:

```bash
device list
station wlan0 scan
station wlan0 get-networks
station wlan0 connect "NomeDaRede"
```

Digite a senha da rede quando solicitado.

Depois saia:

```bash
exit
```

Teste:

```bash
ping archlinux.org
```

---

# 3. Atualize o relógio

```bash
timedatectl set-ntp true
```

---

# 4. Inicie o instalador

Execute:

```bash
archinstall
```

O instalador abrirá um menu interativo.

---

# 5. Configure a instalação

Preencha as opções conforme desejar.

## Idioma

Escolha o idioma da instalação.

---

## Espelhos (Mirrors)

Selecione os mirrors mais próximos do seu país.

---

## Discos

Escolha o disco onde o Arch Linux será instalado.

> **Atenção:** O disco será formatado.

---

## Sistema de arquivos

Recomendado:

- **Btrfs** (mais moderno)
- **Ext4** (mais simples e compatível)

---

## Bootloader

Recomendado:

- **GRUB** (compatibilidade)
- **systemd-boot** (UEFI)

---

## Swap

Você pode:

- Criar uma partição Swap;
- Criar um Swapfile;
- Não utilizar Swap.

---

## Hostname

Defina o nome do computador.

Exemplo:

```
archlumix
```

---

## Usuário

Crie seu usuário.

Defina:

- Nome
- Senha
- Permissão de administrador (sudo)

---

## Senha do root

Defina uma senha para o usuário root.

---

## Perfil (Profile)

Escolha o tipo de instalação.

Exemplo:

- Desktop
- Minimal
- Server

---

## Ambiente gráfico (Desktop)

Caso escolha Desktop, selecione um ambiente gráfico.

Algumas opções:

- GNOME
- KDE Plasma
- XFCE
- Cinnamon
- MATE
- LXQt

---

## Driver de vídeo

Selecione o driver correspondente ao seu hardware.

Exemplos:

- Intel
- AMD
- NVIDIA
- VMware
- VirtualBox

---

## Kernel

Recomendado:

- Linux (padrão)
- Linux LTS (mais estável)

---

## Áudio

Recomendado:

```
PipeWire
```

---

## Rede

Recomendado:

```
NetworkManager
```

---

## Pacotes adicionais

Opcionalmente, instale programas extras.

Exemplos:

- git
- vim
- firefox
- htop
- wget
- curl
- unzip

---

# 6. Revise as configurações

Antes de instalar, confira todas as opções.

Se estiver tudo correto, selecione:

```
Install
```

A instalação poderá levar alguns minutos.

---

# 7. Finalizando

Quando o processo terminar:

Remova o pendrive.

Reinicie:

```bash
reboot
```

Faça login utilizando o usuário criado durante a instalação.

---

# ✅ Após a instalação

É recomendado:

- Atualizar o sistema:
  ```bash
  sudo pacman -Syu
  ```

- Instalar o AUR Helper (`yay`);

- Configurar o firewall;

- Instalar codecs multimídia;

- Instalar fontes adicionais;

- Configurar backups;

- Personalizar o ambiente gráfico.

> **🎉 Parabéns!** Seu Arch Linux foi instalado com sucesso utilizando o **archinstall** e está pronto para ser configurado conforme suas necessidades.

# Pós-instalação: componentes essenciais

Para que o Arch Linux funcione corretamente após a instalação, alguns serviços e componentes devem estar instalados e habilitados.

> **⚠️ Observação:** Alguns desses itens já podem ter sido instalados automaticamente pelo `archinstall`, dependendo das opções escolhidas.

---

## 1. Atualize o sistema

Antes de qualquer configuração, atualize todos os pacotes.

```bash
sudo pacman -Syu
```

---

## 2. Habilite o NetworkManager

Responsável pela conexão com a internet.

```bash
sudo systemctl enable --now NetworkManager
```

---

## 3. Instale os microcódigos da CPU

### Intel

```bash
sudo pacman -S intel-ucode
```

### AMD

```bash
sudo pacman -S amd-ucode
```

---

## 4. Instale os drivers de vídeo

Escolha o driver correspondente ao seu hardware.

### Intel

```bash
sudo pacman -S mesa vulkan-intel
```

### AMD

```bash
sudo pacman -S mesa vulkan-radeon
```

### NVIDIA

```bash
sudo pacman -S nvidia nvidia-utils
```

---

## 5. Instale fontes básicas

```bash
sudo pacman -S noto-fonts noto-fonts-emoji ttf-dejavu
```

---

## 6. Habilite o Bluetooth (Opcional)

Caso seu computador possua Bluetooth:

```bash
sudo systemctl enable --now bluetooth
```

---

## 7. Verifique o áudio

O recomendado é utilizar o **PipeWire**, que normalmente já é instalado pelo `archinstall`.

---

## 8. Reinicie o computador

Após instalar ou alterar componentes importantes:

```bash
reboot
```

---

# Uma dica

Baixe a ferramenta `Linux Toys` para baixar outras configurações adicionais, como aplicativos, IDE's, etc…

  <img src="https://linux.toys/elements/linuxtoys.webp" width="70">

> **✅ Pronto!** Com esses componentes instalados e habilitados, o Arch Linux estará preparado para funcionar corretamente e você poderá prosseguir com a personalização e instalação dos seus programas.

>  **❗️ Atenção** Este repositório abrange apenas um pouco do assunto. Caso queira saber mais sobre, é recomendável pesquisar em outras plataformas/repositórios para saber mais.
