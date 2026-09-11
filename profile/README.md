<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/B002-FUTURE-LAB/Img/main/svg/logo-dark.svg">
    <img src="https://raw.githubusercontent.com/B002-FUTURE-LAB/Img/main/svg/logo.svg" alt="B002 Future Lab" width="420">
  </picture>
</p>

<p align="center">
  <b>A mobile base and an arm, working in the same map.</b><br>
  Applied robotics in lab B002 — ROS 2 Jazzy, autonomous navigation and manipulation.
</p>

---

## What happens here

B002 is a lab with two real robots and one interesting problem: getting them to
understand each other. A **TurtleBot4** navigates the room's map on its own; a
**MyCobot** does pick & place with vision. Apart, each one is a tutorial.
Together — sharing one coordinate frame and one 3D view — they become a work
cell, and that's where the actual work is.

All of it runs on physical hardware, not just in simulation. Dock/undock,
RPLidar, OAK-D, flaky Wi-Fi and sensors that take their time coming back after
an undock are all part of the scope.

## The three systems

| | What it does | Stack |
|---|---|---|
| 🟢 **TurtleBot4** | navigates the B002 map autonomously, with a waypoint delivery routine | ROS 2 Jazzy, Nav2, AMCL, RPLidar, OAK-D |
| 🦾 **MyCobot** | plans and executes arm motion; pick & place with vision-based detection and a suction pump | MoveIt, Docker, YOLO, GPIO |
| 🧩 **Integration** | anchors the arm in the map (`map → mycobot_base_link`), bridges the joints, and draws both robots in one RViz 3D view | ROS 2, TF2, RViz |

The three move together as submodules in the aggregator repository — that's
where it's recorded which version of each one works with which:

### 👉 [**B002_Future_Lab_Bots**](https://github.com/MHC-CodeSmith/B002_Future_Lab_Bots)

```bash
git clone --recurse-submodules https://github.com/MHC-CodeSmith/B002_Future_Lab_Bots.git
```

Its README carries the operating walkthrough: the three Terminator windows, the
order to bring things up (localization → Nav2 → visualization), and the mission
manager.

## Brand assets

Logo, icon, palette and usage rules live in [**Img**](https://github.com/B002-FUTURE-LAB/Img)
— one place, so loose copies of the logo don't end up scattered everywhere.

<p align="center">
  <img src="https://raw.githubusercontent.com/B002-FUTURE-LAB/Img/main/png/icon-128.png" alt="Symbol" width="72">
</p>

<p align="center">
  <sub>The symbol is the whole lab: the circle is the TurtleBot4 seen from above with the LIDAR on its axis,<br>
  the two segments are the MyCobot arm, and the green dot is the end effector.</sub>
</p>

---

<p align="center">
  <sub>B002 Future Lab · TurtleBot4 · MyCobot · ROS 2 Jazzy</sub>
</p>
