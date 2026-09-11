<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/B002-FUTURE-LAB/Img/main/svg/logo-dark.svg">
    <img src="https://raw.githubusercontent.com/B002-FUTURE-LAB/Img/main/svg/logo.svg" alt="B002 Future Lab" width="420">
  </picture>
</p>

<p align="center">
  <b>Uma base móvel e um braço, trabalhando no mesmo mapa.</b><br>
  Robótica aplicada no laboratório B002 — ROS 2 Jazzy, navegação autônoma e manipulação.
</p>

---

## O que rola aqui

O B002 é um laboratório com dois robôs reais e um problema interessante: fazer
os dois se entenderem. Um **TurtleBot4** navega sozinho pelo mapa da sala; um
**MyCobot** faz pick & place com visão. Sozinhos, cada um é um tutorial. Juntos,
compartilhando o mesmo sistema de coordenadas e a mesma visualização 3D, viram
uma célula de trabalho — e é aí que está o trabalho de verdade.

Tudo roda em hardware físico, não só em simulação. Dock/undock, RPLidar, OAK-D,
Wi-Fi instável e sensores que demoram a voltar depois do undock fazem parte do
escopo.

## Os três sistemas

| | O que faz | Stack |
|---|---|---|
| 🟢 **TurtleBot4** | navega autônomo pelo mapa do B002, com rotina de delivery por waypoints | ROS 2 Jazzy, Nav2, AMCL, RPLidar, OAK-D |
| 🦾 **MyCobot** | planeja e executa movimentos do braço; pick & place com detecção por visão e bomba de vácuo | MoveIt, Docker, YOLO, GPIO |
| 🧩 **Integração** | ancora o braço no mapa (`map → mycobot_base_link`), faz a ponte de juntas e desenha os dois no mesmo RViz 3D | ROS 2, TF2, RViz |

Os três andam juntos como submódulos no repositório agregador — é lá que fica
registrado qual versão de cada um funciona com qual:

### 👉 [**B002_Future_Lab_Bots**](https://github.com/MHC-CodeSmith/B002_Future_Lab_Bots)

```bash
git clone --recurse-submodules https://github.com/MHC-CodeSmith/B002_Future_Lab_Bots.git
```

O README de lá tem o passo a passo de operação: as três janelas do Terminator,
a ordem de subir localização → Nav2 → visualização, e o mission manager.

## Identidade visual

Logo, ícone, paleta e regras de uso vivem em [**Img**](https://github.com/B002-FUTURE-LAB/Img)
— um lugar só, pra não espalhar cópia solta de logo por aí.

<p align="center">
  <img src="https://raw.githubusercontent.com/B002-FUTURE-LAB/Img/main/png/icon-128.png" alt="Símbolo" width="72">
</p>

<p align="center">
  <sub>O símbolo é o laboratório inteiro: o círculo é o TurtleBot4 visto de cima com o LIDAR no eixo,<br>
  os dois segmentos são o braço do MyCobot, e o ponto verde é o efetuador.</sub>
</p>

---

<p align="center">
  <sub>B002 Future Lab · TurtleBot4 · MyCobot · ROS 2 Jazzy</sub>
</p>
