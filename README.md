# Oficina de Impressão 3D — Quarto + Reveal.js

Apresentação editável para uma oficina presencial de 180 minutos. A fonte principal é `oficina_impressao_3d.qmd`; os diagramas ficam em `recursos/` e o tema em `custom.scss`. A prática usa PrusaSlicer portátil para Windows e o modelo 3DBenchy em STL.

## Renderizar

Com Quarto instalado:

```bash
quarto render oficina_impressao_3d.qmd
```

O comando gera `oficina_impressao_3d.html`. O YAML usa `embed-resources: true`, portanto o HTML pode ser copiado para outro computador e aberto sem internet.

## Apresentar

Abra o HTML no Chrome/Chromium e use tela cheia (`F`). As notas ficam disponíveis na visão do apresentador (`S`). Navegação: setas, espaço ou clique. O conteúdo foi dimensionado para 16:9 e projetor.

## Editar

Altere o QMD e, se necessário, os SVGs em `recursos/`. Evite caminhos absolutos. Os diagramas são SVG válidos e são incorporados no HTML durante a renderização.

## Validação rápida

```bash
quarto check
rg -n 'src="(https?://|[^d][^"]+\.(png|jpg|svg))' oficina_impressao_3d.html
```

O segundo comando deve retornar vazio para imagens externas; recursos locais incorporados aparecem como `data:` no HTML final.

## Créditos das fotografias

As fotografias estão em `recursos/fotos/` e são incorporadas localmente no HTML. As páginas-fonte e licenças são mantidas nos créditos dos slides:

- FDM: [3D-PRINTER.jpg](https://commons.wikimedia.org/wiki/File:3D-PRINTER.jpg), CC BY 4.0, Mustafa Al-Elq.
- Resina: [Elegoo mars.jpg](https://commons.wikimedia.org/wiki/File:Elegoo_mars.jpg), CC BY 2.0, Tampere Hacklab.
- SLS: [Sharebot SnowWhite SLS](https://commons.wikimedia.org/wiki/File:3D_Printshow_2014_London_-_Sharebot_SnowWhite_SLS_3D_printer_v04_(15147924241).jpg), CC BY 2.0, Creative Tools.
- Usinagem: [CNC milling machine.jpg](https://commons.wikimedia.org/wiki/File:CNC_milling_machine.jpg), CC BY-SA 4.0, Impressionmanufacturer.
- Injeção: [Injection moulding machine.jpg](https://commons.wikimedia.org/wiki/File:Injection_moulding_machine.jpg), CC BY-SA 3.0, Rohini.
- Creality: [Ender 3x 3D printer kit](https://commons.wikimedia.org/wiki/Category:Creality_Ender_3), Wikimedia Commons.
- Bambu Lab: [Bambu Lab X1 Carbon with AMS module](https://commons.wikimedia.org/wiki/File:Bambu_Lab_X1_Carbon_with_AMS_module.jpg), CC BY-SA 4.0, Benlisquare.
- Filamento: [3D-Druck-Filament in verschiedenen Farben](https://commons.wikimedia.org/wiki/File:3D-Druck-Filament_in_verschiedenen_Farben.jpg), Wikimedia Commons.
- Resina pós-impressão: [Résultat d’une impression 3D avant nettoyage](https://commons.wikimedia.org/wiki/File:R%C3%A9sultat_d%E2%80%99une_impression_3D_avant_nettoyage.jpg), Wikimedia Commons.
- CNC robotizada: [EGU-Metall CNC-Fräsen mit Roboterautomatisierung](https://commons.wikimedia.org/wiki/File:EGU-Metall_CNC-Fr%C3%A4sen_mit_Roboterautomatisierung.jpg), Wikimedia Commons.
- Injeção robotizada: [Injection Molding Machine with a robot arm](https://commons.wikimedia.org/wiki/File:Injection_Molding_Machine_with_a_robot_arm.jpg), Wikimedia Commons.
- Componentes: [Hotend.jpg](https://commons.wikimedia.org/wiki/File:Hotend.jpg), [Printer Baseboard PCB.jpg](https://commons.wikimedia.org/wiki/File:Printer_Baseboard_PCB.jpg), [Electronics of 3D Printer.jpg](https://commons.wikimedia.org/wiki/File:Electronics_of_3D_Printer.jpg) e [Y-axis y-belt and bearing.jpg](https://commons.wikimedia.org/wiki/File:Y-axis_y-belt_and_bearing.jpg). Licenças e autores estão nas respectivas páginas.

## Vídeos recomendados

Os links aparecem também nos slides. Eles são recursos externos e não ficam incorporados no HTML:

- [Como funciona uma impressora FDM](https://www.youtube.com/watch?v=WA9iZ_EzcH4)
- [Comparação FDM, SLA e SLS](https://www.youtube.com/watch?v=4wHonWbx3fo)
- [Introdução à estereolitografia — Formlabs](https://www.youtube.com/watch?v=Ei2HGPhHPCY)
- [Playlist oficial do PrusaSlicer](https://www.prusa3d.com/en/page/prusaslicer_426/)
- [Vídeos da Bambu Lab](https://www.youtube.com/@BambuLab/videos)
- [Vídeos da Haas Automation](https://www.youtube.com/@HaasAutomation/videos)

Para uma oficina sem internet, teste e prepare previamente os vídeos, respeitando as condições de uso e direitos autorais.
