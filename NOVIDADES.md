# Novidades do port

O Otavix Launcher mostra este arquivo na página "Novidades" do jogo. Cada atualização tem um título
"## <data> · <versão>" e o texto em português (### pt), inglês (### en) e espanhol (### es). As mais novas ficam em cima.

## 27/11/2026 · 0.1.5
### pt
- **Save state de volta no Blade II**, corrigido: F5 salva, F8 carrega, F6/F7 trocam o espaço (no controle, segure Select e aperte RB / LB). O defeito de imagem ao carregar (texturas com blocos e lixo colorido) foi corrigido no motor PS2 0.1.37.
- **Motor PS2 0.1.37:** o save state ficou mais confiável ao carregar um estado na mesma sessão: agora ele guarda também a textura que estava sendo enviada ao GS e a máscara de profundidade, e as texturas não ficam mais com blocos ou lixo colorido depois da carga. Estados salvos na versão anterior não carregam nesta; o aviso na tela explica.
- **Também no motor 0.1.37:** carregar um estado podia corromper a memória e fechar o jogo, e um dado lido como comando pelo VIF1 podia deixar texturas presas na fila (o salvamento era recusado e a imagem sujava). As duas coisas foram corrigidas.
### en
- **Save states are back in Blade II**, fixed: F5 saves, F8 loads, F6/F7 change the slot (on the controller, hold Select and press RB / LB). The picture defect when loading (textures with blocks and colored garbage) was fixed in PS2 engine 0.1.37.
- **PS2 engine 0.1.37:** save states are more reliable when loading a state in the same session: they now also keep the texture that was being sent to the GS and the depth mask, and textures no longer show blocks or colored garbage after loading. States saved in the previous version do not load in this one; the on-screen notice explains it.
- **Also in engine 0.1.37:** loading a state could corrupt memory and close the game, and data read as a command by the VIF1 could leave textures stuck in the queue (saving was refused and the picture got garbage). Both are fixed.
### es
- **El save state vuelve a Blade II**, corregido: F5 guarda, F8 carga, F6/F7 cambian el espacio (en el mando, mantén Select y pulsa RB / LB). El defecto de imagen al cargar (texturas con bloques y basura de colores) se corrigió en el motor PS2 0.1.37.
- **Motor PS2 0.1.37:** el save state es más fiable al cargar un estado en la misma sesión: ahora guarda también la textura que se estaba enviando al GS y la máscara de profundidad, y las texturas ya no quedan con bloques ni basura de colores después de cargar. Los estados guardados en la versión anterior no cargan en esta; el aviso en pantalla lo explica.
- **También en el motor 0.1.37:** cargar un estado podía corromper la memoria y cerrar el juego, y un dato leído como comando por el VIF1 podía dejar texturas atascadas en la cola (el guardado se rechazaba y la imagen se ensuciaba). Ambas cosas se corrigieron.

## 26/11/2026 · 0.1.4
### pt
- **Save state desligado temporariamente no Blade II** por um defeito de imagem ao carregar (texturas com blocos e lixo colorido depois de carregar um estado na mesma sessão). Volta numa próxima versão, já corrigido. O save do próprio jogo (cartão de memória) continua normal.
### en
- **Save states temporarily turned off in Blade II** because of a picture defect when loading (textures with blocks and colored garbage after loading a state in the same session). They come back in a future version, fixed. The game's own save (memory card) works as before.
### es
- **Save state desactivado temporalmente en Blade II** por un defecto de imagen al cargar (texturas con bloques y basura de colores después de cargar un estado en la misma sesión). Vuelve en una próxima versión, ya corregido. El guardado del propio juego (tarjeta de memoria) sigue igual.

## 25/11/2026 · 0.1.3
### pt
- **Motor PS2 0.1.36:** o primeiro save state da sessão ficou instantâneo (antes levava cerca de 1 s). Estados salvos na versão anterior não carregam nesta; o aviso na tela explica.
### en
- **PS2 engine 0.1.36:** the first save state of a session is now instant (it used to take about 1 s). States saved in the previous version do not load in this one; the on-screen notice explains it.
### es
- **Motor PS2 0.1.36:** el primer save state de la sesión ahora es instantáneo (antes tardaba cerca de 1 s). Los estados guardados en la versión anterior no cargan en esta; el aviso en pantalla lo explica.

## 24/11/2026 · 0.1.2
### pt
- **Salvar e carregar o estado (save state)**, como nos emuladores, em 9 espaços: F5 salva, F8 carrega, F6/F7 trocam o espaço; no controle, segure Select e aperte RB (salvar) ou LB (carregar). Um aviso na tela confirma. Os estados valem para esta versão do port; dá para desligar na página Controles do launcher.
### en
- **Save states**, like in emulators, in 9 slots: F5 saves, F8 loads, F6/F7 change the slot; on the controller, hold Select and press RB (save) or LB (load). An on-screen notice confirms it. States work for this port version; they can be turned off in the launcher's Controls page.
### es
- **Guardar y cargar el estado (save state)**, como en los emuladores, en 9 espacios: F5 guarda, F8 carga, F6/F7 cambian el espacio; en el mando, mantén Select y pulsa RB (guardar) o LB (cargar). Un aviso en pantalla lo confirma. Los estados valen para esta versión del port; se pueden desactivar en la página Controles del launcher.

## 24/11/2026 · 0.1.1
### pt
- A parte gráfica do console passou para a **placa de vídeo**: acabou a travada de cerca de 1 segundo em cenas pesadas e o processador fica mais livre. O texto dos menus continua certo.
### en
- The console's graphics now run on the **GPU**: the roughly 1-second freeze in heavy scenes is gone and the CPU has more headroom. Menu text still comes out right.
### es
- La parte gráfica de la consola pasó a la **tarjeta de video**: se acabó el congelamiento de cerca de 1 segundo en escenas pesadas y el procesador queda más libre. El texto de los menús sigue saliendo bien.

## 24/11/2026 · 0.1.0
### pt
- **Primeira versão jogável (beta).** O port gera o jogo a partir da sua ISO americana (SLUS-20360) e roda do começo: logos, menu, briefing e a primeira fase, a 30 FPS, que é o ritmo do jogo no PlayStation 2. Neste jogo a parte gráfica do console roda no processador, para o texto dos menus sair certo; por isso a resolução interna fica em 1x. Teclado e mouse junto com o controle (teclas trocadas na página Controles do launcher).
### en
- **First playable release (beta).** The port builds the game from your US ISO (SLUS-20360) and runs from the start: logos, menu, briefing and the first level, at 30 FPS, the game's own rate on the PlayStation 2. In this game the console's graphics run on the CPU so the menu text comes out right; that is why the internal resolution stays at 1x. Keyboard and mouse alongside the controller (keys changed in the launcher's Controls page).
### es
- **Primera versión jugable (beta).** El port genera el juego a partir de tu ISO estadounidense (SLUS-20360) y funciona desde el principio: logos, menú, briefing y el primer nivel, a 30 FPS, que es el ritmo del juego en PlayStation 2. En este juego la parte gráfica de la consola funciona en el procesador para que el texto de los menús salga bien; por eso la resolución interna se queda en 1x. Teclado y ratón junto con el mando (teclas cambiadas en la página Controles del launcher).

## 06/11/2026 · 0.0.2
### pt
- O port vai usar o **motor PS2 próprio** do projeto (tradutor e runtime feitos aqui), que o gerador vai baixar pronto.
### en
- The port will use the project's **own PS2 engine** (translator and runtime made here), which the generator will download prebuilt.

## 27/10/2026 · 0.0.1
### pt
- **Página criada.** O port ainda vai começar: primeiro estamos fortalecendo a base comum dos ports de PS2 com os quatro primeiros jogos. Você vai precisar da ISO da versão americana (SLUS-20360).
### en
- **Page created.** The port has not started yet: we are first strengthening the shared PS2 base with the first four games. You will need the American release ISO (SLUS-20360).
