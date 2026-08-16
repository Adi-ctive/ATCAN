# ATCAN specification

Autonomous Trash Collection & Aqua Navigation robot.
Smart India Hackathon 2024, problem statement **SIH1603**. Team ATCAN.

Everything on this page is reconstructed from the September 2024 project
document and the design conversations that produced it. Where a number is
given, it came from the original submission.

---

## Purpose

Collect floating solid waste from the surface of water bodies with no human
operator on board. Target debris is plastic bags, wrappers and bottles.

The problem framing was that manual cleanup works but does not scale. A small
number of people clearing waste by hand cannot cover the surface area involved,
so the task needs to be automated rather than staffed.

---

## Platform

| Property | Value |
|---|---|
| Length x width x height | 2.5 m x 0.75 m x 1.5 m |
| Bare hull mass | 80 kg |
| Component mass budget | 60 kg |
| Maximum speed | 1.5 m/s |
| Power | Solar panels on the roof, battery buffered |
| Float material | Solid HDPE |
| Structure material | PVC |
| Estimated cost | approx. USD 1700 / Rs. 1.4 lakh |
| Autonomy | Fully autonomous, remotely monitored |

Hull form is twin hull with an open channel between the bows. The collection
mouth sits in that channel, so debris is funnelled into the intake as the
vehicle moves forward rather than being pushed aside by a single wide bow.

---

## Sensing and navigation

| Function | Sensor |
|---|---|
| Obstacle detection and avoidance | RADAR |
| Trash detection and identification | Visual camera, AI object detection |
| Position and route following | GPS |
| Collection state | Weight sensors on the collection assembly |

Route following is over pre-defined paths. Object detection identifies floating
debris, the vehicle steers to it, and collection happens on the move.

The weight sensors close the operating loop. When the measured load crosses the
full threshold, the vehicle stops collecting and returns to base to be emptied.
Collection capacity is therefore bounded by mass, not by time or by area covered.

---

## The two collection variants

Two mechanisms were specified rather than one, because the right choice depends
on water conditions.

### ATCAN-CN, Collection Net

A wide net is held with its mouth forward and its body horizontal. Debris is
scooped as the vehicle moves. Water passes through the mesh and the solid waste
is retained.

- Lighter, so less power per unit distance
- Longer operating duration on the same battery and solar budget
- More customisable, the net is a replaceable part
- Best suited to calm water

### ATCAN-CB, Conveyor Box

A mesh conveyor belt lifts debris out of the water and deposits it into a wire
mesh storage box. The mesh drains the load so stored water weight does not
accumulate.

- Heavier, therefore more stable against surface turbulence
- Easier emptying and access at base
- Higher electrical power draw
- Slower, because of the added mass

**Selection rule.** ATCAN-CN is the default for most deployments. ATCAN-CB is
chosen when the water is rough enough that a towed net loses debris or the
vehicle loses attitude stability.

---

## Component layout

Recovered from the construction plan in the submission video. Top view, bow at
the top.

| Position | Component |
|---|---|
| Channel between the bows | The collection net, mesh, held horizontally |
| Port and starboard | The catamaran multi hull, solid HDPE |
| Forward on the body | The visual camera |
| Body roof | RADAR and solar panels |
| Body | Upper frame structure, electrical components, propulsion |
| Stern | Rudder fin for steering, propellers, wheels |

The wheels are not for driving. They are there so the vehicle can be dragged
ashore for emptying and servicing without lifting it.

---

## What was not built

This project stopped at design. There is no control software and no detection
model in this repository, because none were written. The deliverables were the
design document, the 3D models and the submission video.

Both 3D models survive and are linked from the README. The design document does
not.

The engineering content that does survive is the specification above and the
sequence of physical design decisions recorded in
[DESIGN-EVOLUTION.md](DESIGN-EVOLUTION.md).
