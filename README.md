<h1 align="center">Blade II — port nativo para PC</h1>

<p align="center"><i>Blade II (PS2, NTSC-U SLUS-20360): port nativo para PC por recompilação estática, com o motor PS2 próprio do projeto. Gera a partir da sua ISO. Beta.</i></p>

<p align="center">
  <a href="https://github.com/otavix010/blade-2-pc/commits/main"><img alt="Última atualização" src="https://img.shields.io/github/last-commit/otavix010/blade-2-pc?label=%C3%BAltima%20atualiza%C3%A7%C3%A3o"></a>
  <a href="https://github.com/otavix010/otavix-launcher/releases/latest"><img alt="Baixar o Otavix Launcher" src="https://img.shields.io/badge/Otavix%20Launcher-baixar-b00020"></a>
  <img alt="Windows 10/11" src="https://img.shields.io/badge/Windows-10%2F11-0078d4">
  <img alt="Linux: não suportado no momento" src="https://img.shields.io/badge/Linux-n%C3%A3o%20suportado-lightgrey">
</p>

<p align="center">
  <a href="#o-que-é">O que é</a> ·
  <a href="#estado-atual-beta">Estado atual: beta</a> ·
  <a href="#opções">Opções</a> ·
  <a href="#plataformas">Plataformas</a> ·
  <a href="#requisitos">Requisitos</a> ·
  <a href="#desempenho-medido">Desempenho</a> ·
  <a href="#como-gerar">Como gerar</a> ·
  <a href="#perguntas-frequentes">Perguntas frequentes</a> ·
  <a href="#como-funciona">Como funciona</a> ·
  <a href="#english-summary">English</a>
</p>

> **Projeto de fãs, sem fins lucrativos.** *Blade* é marca registrada da Marvel; este projeto não tem relação com a Marvel nem com a Activision. Este repositório **não contém o jogo**: você precisa da **sua própria cópia** do DVD (a versão americana, **SLUS-20360**).

> [!IMPORTANT]
> **Para jogar, baixe o [Otavix Launcher](https://github.com/otavix010/otavix-launcher/releases/latest).** Ele baixa este port, pede a sua ISO, gera o jogo no seu PC e o mantém atualizado. Para relatar um problema ou pedir algo, use **"Reportar problema"** na página do jogo no launcher: o relatório já vai com o log e as configurações, e é por ele que as correções saem mais rápido.
>
> **To play, download the [Otavix Launcher](https://github.com/otavix010/otavix-launcher/releases/latest).** It downloads this port, asks for your ISO, makes the game on your PC and keeps it updated. To report a problem or ask for something, use **"Report a problem"** on the game's page in the launcher: the report carries the log and the settings, and that is how fixes come out fastest.

[English summary below](#english-summary)

## O que é

Um port **nativo** do *Blade II* (PlayStation 2, 2002) para Windows. Não é um emulador: o código do jogo é **traduzido para C++ e compilado** para x86-64 (recompilação estática), com o motor PS2 próprio do projeto (Otavix).

Como o código do jogo não pode ser distribuído, **o seu PC gera e compila a parte do jogo a partir da sua ISO**. Um comando só faz tudo.

## Estado atual: beta

O jogo roda do começo: logos, menu, briefing da missão e a primeira fase (o galpão do treino), **a 30 FPS, que é o ritmo do jogo no PlayStation 2** (testado num Ryzen 7 9800X3D). Os microprogramas de geometria do VU1 são traduzidos para C++ na sua máquina (a etapa "VU1" do gerador). A parte gráfica do console (GS) roda na **placa de vídeo**.

É a primeira versão: o jogo ainda não foi jogado até o fim no port; só a primeira fase foi testada. Relate pelo launcher o que encontrar.

## Opções

Pelo [Otavix Launcher](https://github.com/otavix010/otavix-launcher/releases/latest), no menu de opções do jogo: janela ou **tela cheia** (no jogo, F11 ou Alt+Enter alternam), tamanho da janela, escalonador (**bilinear, AMD FSR 1 ou NVIDIA Image Scaling**) e a nitidez dele, anti-serrilhamento **FXAA** e predefinições. A **resolução interna** (2x e 4x) ainda não foi testada neste jogo: por enquanto ele fica em 1x. A imagem fica em 4:3 (sem tela larga por enquanto). Sem o launcher, as mesmas opções são variáveis de ambiente: `PS2X_TELA_CHEIA=1`, `PS2X_JANELA_TAM=1920x1080`, `PS2X_ESCALA=nenhum|bilinear|fsr|nis`, `PS2X_NITIDEZ_PCT=0..100`, `PS2X_FXAA=1`.

## Teclado e mouse

O teclado e o mouse funcionam junto com o controle. As teclas são trocadas na página **Controles** do
[Otavix Launcher](https://github.com/otavix010/otavix-launcher/releases/latest), que também liga ou desliga o teclado e o mouse e ajusta a sensibilidade. Teclas padrão:

| Botão do PlayStation 2 | Tecla padrão |
|---|---|
| Analógico esquerdo | W A S D |
| Analógico direito | mouse (ou I J K L) |
| Direcional | setas |
| X | Espaço ou X |
| Bola | C ou Esc |
| Quadrado | botão esquerdo do mouse ou Z |
| Triângulo | botão direito do mouse ou V |
| L1 / R1 | Q / E |
| L2 / R2 | Shift esquerdo / Shift direito |
| L3 / R3 | F / botão do meio do mouse |
| START / SELECT | Enter / Tab |

No *Blade II* o analógico direito é o ataque: com o mouse, o movimento do mouse vira o golpe. Se preferir, troque as teclas na página **Controles**. O ponteiro do mouse só fica preso na janela depois da primeira tecla do jogo; Alt+Tab solta. F10 (medidor de desempenho), F11 e Alt+Enter (tela cheia) continuam sendo atalhos do port. Sem o launcher: `PS2X_TECLADO=0|1`, `PS2X_MOUSE=0|1`, `PS2X_MOUSE_SENS=5..200` e `PS2X_TECLAS="cross=space;square=mouse1 j;lstick_up=w"` (botão=teclas, separados por `;`).

## Plataformas

| | **Windows** | **Linux / SteamOS** |
|---|---|---|
| Situação | **beta** (este port) | **não suportado no momento** |
| Como jogar | pelo launcher, ou `gerar.cmd` e `jogar.cmd` | só o port de *God of War: Ascension* tem versão Linux (beta) por enquanto |

## Requisitos

- **Windows 10/11 64 bits**, com o **Visual Studio 2022 Build Tools** (C++ e CMake; o comando está em [Como gerar](#como-gerar)). O launcher confere isso para você.
- A **sua ISO** do *Blade II*, na versão americana (NTSC-U) (**SLUS-20360**). O gerador confere o executável e, se não bater, diz se é outra edição (outra região ou versão) ou o mesmo disco modificado.
- **Memória:** o gerador usa uns 3 GB de RAM por compilação em paralelo e escolhe o paralelismo pela memória livre; com pouca RAM funciona, só demora mais.
- **Disco:** uns 10 GB livres para os arquivos do disco, o código traduzido e a compilação.
- **AVX2 não é obrigatório**: o gerador detecta a CPU e usa as bibliotecas AVX2 ou SSE4.

## Desempenho medido

FPS de jogo, no motor 0.1.33, em resolução interna 1x (quadros que o jogo de fato produz, contados no motor). O jogo é feito para 30 FPS no PlayStation 2. **Só colocamos o que foi medido**; as demais máquinas ainda não foram testadas com este jogo.

| Máquina | CPU | GPU | FPS |
|---|---|---|---|
| **PC 1** | Ryzen 7 9800X3D | RTX 5080 | 30 (o limite do jogo; primeira fase) |
| **PC 2** | Core i5-11400F | RX 9060 XT | não medido |
| **Notebook** | Core i5-10300H (4/8) | GTX 1650 | não medido |
| **Portátil** | Legion Go S (Linux) | Radeon 780M | não suportado |

## Problemas conhecidos

- Primeira versão: só a primeira fase foi testada no port.
- Às vezes a lista do menu de controles aparece com letras trocadas.
- Às vezes, por um quadro, o ícone da arma no canto da tela aparece duplicado sobre um retângulo rosado.
- Sem tela larga (16:9) por enquanto.
- Esta é a **versão americana (NTSC-U)** apenas (SLUS-20360); outras regiões e versões são recusadas pelo gerador, com o motivo.

## Como gerar

### Pelo Otavix Launcher

O [Otavix Launcher](https://github.com/otavix010/otavix-launcher/releases/latest) lista este port: ele baixa o port, pede a ISO, gera o jogo e abre.

### À mão

**1. O que você precisa ter:** a sua cópia do *Blade II* **americano** (SLUS-20360, "Blade II (USA)") como imagem **.iso** do DVD (ou .bin/.img de setores brutos). O gerador confere o executável pelo hash: outras versões não servem, porque o mapa de funções é o da americana.

**2. Instale as ferramentas (uma vez só)**, num terminal:
```
winget install Microsoft.VisualStudio.2022.BuildTools --override "--quiet --wait --add Microsoft.VisualStudio.Workload.VCTools --add Microsoft.VisualStudio.Component.VC.CMake.Project --add Microsoft.VisualStudio.Component.VC.Llvm.Clang --includeRecommended"
```
O resto o gerador baixa sozinho: o motor do port (pacote pronto, conferido pelo SHA-256) e o FFmpeg (LGPL). Não precisa de Python nem de Git.

**3. Baixe este repositório** (botão *Code > Download ZIP*, ou `git clone`) e extraia numa pasta **sem espaços no caminho**, por exemplo `C:\blade-2`. Deixe uns 10 GB livres nesse disco.

**4. Clique duas vezes em `gerar.cmd`** e escolha a ISO. Ele:
- confere a ISO e extrai os arquivos do disco para `trabalho\disc`;
- baixa o motor do port (pacote pronto, conferido pelo SHA-256);
- traduz o código do jogo e os microprogramas do VU1 para C++ (só no seu PC);
- compila o código do jogo (de 3 a 30 minutos, conforme o PC; precisa de 16 GB de RAM ou mais).

**5. Jogue com `jogar.cmd`.** O jogo lê os arquivos de `trabalho\disc` e a ISO no lugar onde ela estava na geração (se mudar a ISO de lugar, rode `gerar.cmd -RefazerDe 2`).

Depois de atualizar o port, `gerar.cmd -RefazerDe 3` baixa o motor novo, retraduz e recompila sem extrair o disco de novo.

## Perguntas frequentes

**Este repositório tem o jogo?** Não. Você precisa da sua própria cópia do DVD; o gerador monta o port no seu PC a partir da sua ISO.

**Por que 30 FPS?** É o ritmo do *Blade II* no PlayStation 2: o jogo espera duas atualizações da tela por quadro. O port segue o original.

**Roda no Linux ou no SteamOS?** Ainda não: só o port de *God of War: Ascension* tem versão Linux (beta). Este roda no Windows.

**O gerador disse "executável modificado" ou "edição diferente". E agora?** "Edição diferente" é outra região ou versão do disco; "executável modificado" é o mesmo disco com o executável alterado (patch, tradução, hack ou ISO danificada). Use uma cópia original sem modificações (SLUS-20360).

**Saiu uma atualização do port. O que faço?** Atualize pelo launcher e gere de novo (`gerar.cmd -RefazerDe 3` à mão): ele baixa o motor novo, retraduz e recompila sem extrair o disco de novo.

**Onde relato um problema?** No launcher, em **"Reportar problema"** na página do jogo.

## Como funciona

- **O motor** (tradutor MIPS R5900 → C++ e runtime: GS, VU1, DMA, IOP, áudio SPU2, cartão de memória) é próprio do projeto e vem pronto (bibliotecas compiladas); o seu PC só traduz e compila o código do jogo.
- **O mapa de funções** (`jogo\ghidra_funcoes.csv`) veio de uma análise com o [Ghidra](https://ghidra-sre.org/) e a extensão ghidra-emotionengine-reloaded: são só endereços e nomes, nada do código do jogo. `jogo\entradas_extra.txt` lista funções chamadas só por ponteiro e alvos de tabelas de salto que a análise não marcou.
- **A receita do VU1** (`jogo\vu1_receita.json`) diz onde os microprogramas de geometria ficam no executável (offsets e tamanhos, conferidos por SHA-1) e como montar a memória de código do VU1.
- **O ritmo do jogo** segue o relógio do PC (`PS2X_RELOGIO_REAL=1` no `jogo\jogo.json`). A geometria do VU1 roda na mesma thread do jogo (`PS2X_MTVU=0`) e o GS roda na placa de vídeo.

## Licença e créditos

- **O nosso código** (`gerar.ps1`, `gerar.cmd`): [MIT](LICENSE).
- **O motor do port** (pacote `otx-motor-ps2`, baixado pronto pelo gerador) não é coberto pela licença MIT; os avisos de terceiros dele (raylib e glfw: zlib; FFmpeg: LGPL, DLLs à parte) estão no `TERCEIROS.txt` do pacote.
- O NIS vem do [NVIDIA Image Scaling SDK](https://github.com/NVIDIAGameWorks/NVIDIAImageScaling) (MIT) e o FSR 1 do [AMD FidelityFX FSR](https://github.com/GPUOpen-Effects/FidelityFX-FSR) (MIT).
- O ícone vem da capa do jogo no [libretro-thumbnails](https://github.com/libretro-thumbnails/Sony_-_PlayStation_2).
- *Blade* é marca registrada da Marvel. Este é um projeto de fãs, sem fins lucrativos, sem relação com a Marvel nem com a Activision e não endossado por elas.

## English summary

A **native PC port** of *Blade II* (PlayStation 2, 2002) made by **static recompilation** with the project's own PS2 engine. **Beta, first release.** It runs from the start (logos, menu, mission briefing and the first level) at **30 FPS, the game's own rate on the PlayStation 2**; only the first level has been tested in the port so far. The console's graphics chip (GS) runs on the **GPU**; the internal resolution stays at 1x for now (not tested in this game yet). Options in the launcher: window or fullscreen (F11 / Alt+Enter), window size, upscaler (bilinear, AMD FSR 1, NVIDIA Image Scaling) and sharpness, FXAA. The picture stays 4:3. Keyboard and mouse work alongside the controller.

**Platforms:** Windows 10/11 only for now (Linux is not supported yet; only the *God of War: Ascension* port has a Linux beta). **Easiest: the [Otavix Launcher](https://github.com/otavix010/otavix-launcher/releases/latest).**

**Bring your own game**: no game code or data here, only the function map (addresses), translation settings and the VU1 "recipe" (offsets and sizes). You need the **US** release (SLUS-20360, Redump "Blade II (USA)") as an **.iso**. Install Visual Studio 2022 Build Tools with C++, CMake and Clang (command above), download this repository to a path without spaces with about 10 GB free, double-click **`gerar.cmd`** (it checks your ISO, extracts the disc files, downloads the prebuilt engine package (no Git needed), translates the game code on your PC and builds it, in 3 to 30 minutes; 16 GB of RAM needed), then play with **`jogar.cmd`**.

License: our scripts are MIT; the engine package is not covered by it, and its third-party notices are in its `TERCEIROS.txt`. *Blade* is a trademark of Marvel; this is a non-commercial fan project, not affiliated with or endorsed by Marvel or Activision.
