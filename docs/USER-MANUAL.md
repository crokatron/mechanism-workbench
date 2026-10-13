# Mechanism Workbench — visual user manual

[Project overview](../README.md) · [Offline interactive demo](../demo.html)

Start with the numbered picture guide. Each number identifies the exact highlighted control. Work through one step at a time; the longer reference is below it.

### Actual tool · controls at a glance

Actual application screenshot. Numbered boxes point to the controls described below. 

![Mechanism Workbench — numbered controls](images/guide-1.jpg)

1. **Find a mechanism.** Search the library or narrow it by category.
2. **Switch the engineering view.** Move between the designer, stress checks and equations/assumptions.
3. **Inspect the full motion.** Move through the opening range and read the clearance and sizing checks.

### Try the working offline example

Screenshot of this project’s interactive demo. Side-by-side services are explicitly simulated.

![Mechanism Workbench — numbered controls](images/guide-2.jpg)

1. **Move the crank.** Use the angle slider to move the solved example.
2. **Change a link length.** The rod changes slider position while preserving the simple linkage.
3. **Read the response.** This smaller demo solves slider-crank motion, not the full door/stress suite.

## Detailed task reference

### Compare a mechanism

1. Search by name or choose a category, then select a built-in mechanism.
2. Read the description and open Equations & assumptions before changing inputs. Note units and whether the model is quasi-static.
3. Change one dimension or load and compare the diagram and result. Save as defaults only when you want the new baseline on this device.

### Work through a hydraulic four-bar door

1. Open Hydraulic four-bar door and the Door designer tab. Identify fixed O–D, input O–A, coupler A–B and output D–B. The moving virtual pivot C is not a physical hinge.
2. Set door geometry and cylinder dimensions, then move the opening-angle slider through the complete motion. Drag the allowed cylinder mount/lug points when exploring placement.
3. Read each geometry and sizing check: loop closure, hardware height, skin clearance, stroke, dead-centre avoidance and pressure. A green result for one check does not clear the others.
4. Use peak load in stress checks and inspect the Stress & strain tab. Export Motion CSV to examine the sampled movement.

### Keep a comparison you can revisit

1. Use Export before substantially changing your defaults. Import the saved workspace to restore it.
2. Name your files by mechanism and purpose; retain the input assumptions alongside any CSV you share.
3. Use Linkage Studio for its dedicated editing workflow. Final pin reactions, lateral clearances, hoses, fasteners and 3D packaging need separate design work.

## Keep your work

Defaults are browser-local. Export/import carries the workspace between devices. A CSV records motion results but does not necessarily preserve every editable setting.

## If something looks wrong

- Impossible linkage: check link lengths, branch selection and closure through the whole range.
- Large pressure spike: inspect leverage and proximity to a dead centre.
- Saved defaults appear different: confirm the same browser/origin or import the intended export.

## What this manual does not promise

The door preview uses sampled motion and conservative envelopes. It does not certify collisions or strength of a finished 3D assembly. The screenshot uses the included editable example, whose dimensions are explicitly unconfirmed.

Screenshots show the actual application where captured. The offline demo is a deliberately smaller simulation and identifies its dummy services. It never controls devices, sends notifications, uploads files or launches printing.
