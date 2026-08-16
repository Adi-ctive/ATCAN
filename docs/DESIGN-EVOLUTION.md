# Design evolution

The hull form was not specified up front. It arrived through three corrections
made on 5 September 2024, each one replacing a general shape with a physical
constraint. The corrections are quoted verbatim from the design session.

---

## Starting point

A cuboidal body with a space at the front for a net, a grey floating bottom
section and a green upper body carrying solar panels. Two top view drawings were
drawn by hand first and used as the input to the design work.

Both drawings are in [`../assets/drawings/`](../assets/drawings/).

---

## Correction 1 — floats are solid, not inflatable

> "the floating area is made of solid hdpe material rather than inflatable balls"

Inflatable flotation is lighter per unit of buoyancy, but a vehicle whose job is
to drive into floating debris will eventually drive into something sharp. A
puncture on an inflatable float is a total loss of the platform. Solid HDPE
trades weight for a failure mode that does not sink the vehicle.

This is a survivability decision, not a buoyancy decision.

---

## Correction 2 — the net is horizontal with the mouth forward

> "the net is supposed to be placed horizontally with the mouth of the net in
> front to collect the trash"

A net hung vertically filters water. A net held horizontally with its mouth
facing forward skims the surface layer, which is where the target debris
actually floats. Plastic bags, wrappers and bottles sit at the interface, so the
intake has to be at the interface too.

It also means collection happens from forward motion alone. There is no
separate actuator for the net on the CN variant.

---

## Correction 3 — hulls with a space between them

> "the floating base is supposed to be a hull like shape with space in between"

This is the decision that produced the final form, and it rejected the cuboid
the design started from.

A single wide flat bow pushes a bow wave ahead of itself. Floating debris rides
that wave outward and away from the vehicle, so the target is displaced by the
approach. Two narrow hulls with an open channel between them do the opposite.
The water between the hulls is undisturbed relative to the vehicle, so debris
stays in the channel and is delivered to the intake.

The catamaran layout also gives a wide beam for roll stability without a wide
wetted bow, which matters because the CB variant carries a heavy conveyor high
above the waterline.

**The result:** twin HDPE hulls, an open channel between the bows, the intake in
the channel, and the body and solar deck aft of the channel. That is the layout
shown in the two drawings.

---

## Why this sequence is the point

Each correction is the same move. A shape gets proposed, and it gets replaced by
a statement about what the water and the debris will physically do to that
shape. Puncture risk, where the target floats, what a bow wave does to something
floating in front of it.

None of the three came from a simulation or a test. They came from reasoning
about the operating environment before anything was committed to.
