# GP5 Controller — pedalboard edition

Interface web independente para controlar a Valeton GP-5, com visual de pedalboard.

## Recursos
- Conexão Bluetooth (Web Bluetooth + SysEx) e USB MIDI, herdadas do projeto-base.
- Nove atalhos de preset (01–09, mapeados inicialmente aos presets internos 00–08).
- Footswitch de Delay para ligar/desligar o bloco DLY.
- Tap Tempo que calcula a colcheia pontuada (75% do tempo de semínima) e envia o tempo ao parâmetro Time do Delay por Bluetooth.
- Interface avançada original para editar os blocos de efeitos.

## Como usar
1. Abra a página publicada pelo GitHub Pages em Chrome ou Edge.
2. Selecione Bluetooth e clique em Connect; ou escolha USB para Web MIDI.
3. Autorize o acesso ao dispositivo e selecione a GP-5.
4. Use os nove botões para chamar os presets 01–09.
5. Toque em TAP TEMPO acompanhando a música. São necessários pelo menos dois toques; os intervalos recentes são usados para suavizar o cálculo.

## Limitações e validação
- Tap Tempo envia o parâmetro de tempo via SysEx Bluetooth. Não está implementado para USB MIDI.
- O tempo calculado é limitado a 20–1000 ms, conforme a configuração do efeito; o intervalo efetivo também depende do modelo de Delay carregado.
- **O Tap Tempo desta adaptação ainda precisa ser testado fisicamente na GP-5.** Não o considere validado até esse teste.
- Os testes anteriores de conexão, seleção de presets, Delay e Drive foram relatados pelo usuário em uma versão de controlador testada anteriormente; não equivalem a uma validação desta adaptação.

## Publicar/atualizar
No GitHub, abra **Settings → Pages**, escolha **Deploy from a branch**, selecione `main` e `/(root)`, e salve. O endereço da página aparece nessa mesma seção quando o deploy terminar.

## Créditos
Esta versão adapta a interface e o código de comunicação do projeto **GP-5 Web Controller**, de Helvecio B. Leal Neto:
https://github.com/helvecioneto/gp5-wc

Consulte `LICENSE` e `ATTRIBUTION.md`. Projeto independente, sem afiliação ou endosso da Valeton.
