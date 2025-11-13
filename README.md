# Bench-Scale Electrochemical Flow Cell Build
Build your own flow cell, for use in standardized flow battery and slurry electrode experimental systems. Can use electrolyte chamber for half cell measurements or two of the same for full cell measurements. 

**NOTE: This is precariously maintained/documented and very much a work in progress. Please feel free to reach out to me at mshahabuddin [at] wpi [dot] edu for any questions if attempting to build before fully documented.**

<img width="875" height="543" alt="image" src="https://github.com/user-attachments/assets/6a9ba918-f67a-4ed7-871c-6386833f79b3" />


## Bill of Materials 
### In this repo:
- 1 "Inlet" type plate fabricated per "half cell" tested (i.e. for half cell measurements, only 1 inlet plate required)
- 1 "Cell Channel" type plate fabricated per "half cell" tested. Can adjust cell thickness to resolution of your print.
- 1 "Non conductive plate" type plate fabricated per "half cell tested", unless machining current collector directly
- For half cell measurements, 1 electrolyte chamber
### To purchase
- Separator material (chemistry specific - I typically use a size exclusion/non-ion selective separator. For example a [polypropylene size exclusion separator](https://celgard.shop/collections/all)
- Gasket sheet (I use [silicone](https://www.mcmaster.com/8525T41/). Will need to cut 
- [M4 threaded rods](https://www.mcmaster.com/94185A145/) (or bolts if preferred). Nonconductive material if using graphite plate or metal plate current collector.
- [M4 nuts](https://www.mcmaster.com/94150A335/), I typically use flange nuts but their diameter may be too large for some of the inlet channels.
- IDEX fittings and associated tubing
- 1/8" EPDM O-ring (or material of choice)
- Graphite foil or graphite plate if machining current collector
- Glue (superglue works well, conductive glue would be better)
### Tools
- Hand drill or drill press
- Bench vice
- 1/4"-28 Bottom Tap

## (Non-comprehensive) Instructions
1. Print parts as per the bill of materials.
    - Note filament materials - make sure your printed materials resist your chosen electrolyte materials. In general, PP is resistant to most aqueous electrolytes across a broad range of pHs, but is much more mercurial to print. PLA works fine for most acidic/mild pH electrolytes but will hydrolyze in concentrated base. 
2. Into each printed inlet plate, use the bottom tap to create threading for IDEX fittings
3. Place 1/8" O-rings into threaded holes
    - sometimes the threads will leak even with the IDEX ferrules due to print lines not sitting flush with the ferrule. The O-rings seem to consistently fix this issue even relatively high flowrates/pressure.
4. (for half cell) Cut gasket sheeting for electrolyte chamber
    - can use a vectorized version of the cell channel model to cut using a cutting tool like a Cricut. I usually just use a printed cell channel part and use it as a stencil to cut the flow channel shape out of the gasket sheet. For holes, a typical hole punch works and accommodates M4 bolts well.
5. Cut gasket sheeting for current collector backing
    - Cut outline of "cell channel", but rather than the cutting the full cell channel, cut holes by the inlet and outlet ports of the inlet plate. This will result in a gasket of the same dimensions as the cell channel, but with 8 holes - 6 for each bolt, 2 for the inlet and outlet of the flow channel
5. Cut strip of separator material such that it covers the entire with of the cell channel but fits within the total width between two of the bolts.
6. Taking non-conductive plate print, glue graphite foil to cover at least the portion of the non-conductive plate exposed to the cell channel and at least enough overhang to clip electrical connection to -- this is where your test equipment will connect to your working electrode
7. Sandwich together all components:
    - Half cell will have the following order: "inlet" plate - current collector gasket - "non-conductive" plate - (adhered to) graphite foil - cell channel -> separator sheet -> electrolyte chamber gasket -> electrolyte chamber
    - Full cell will have the following order: "inlet" plate -> current collector gasket -> "non-conductive" plate -> (adhered to) graphite foil -> cell channel -> separator sheet -> cell channel -> graphite foil -> (adhered to) "non-conductive" plate -> current collector gasket -> "inlet" plate
        - Full cell has not been properly leak tested - consider printing the cell channels out of compressible polymers (Shore ~60-70) for better hermetic contact between cell channels. In the worst case (worst because it offers less control over channel thickness), consider using electrolyte chamber gaskets on either side of the separator.
    - The bolts should fit easily through each layer. Nuts will screw on either end and can be tightened to desired torque
8. If that somehow made sense - congratulations! You should have a testable flow cell.

Here is an example image. Note that this is from earlier versions of this project so the geometries of each part may not align with the models. **TODO: include more instructive images/figures for each step.**

<img width="587" height="539" alt="image" src="https://github.com/user-attachments/assets/563a82fb-cc45-4521-85c7-6b396a02817b" />

## Build/compatibility notes
- The cell electrolyte chamber has ~10 mm hole diameters on the top, built to accomodate 9.5 mm OD reference electrodes like from [Pine Research](https://pineresearch.com/products/reference-ag-agcl-standard-single/)
- Note that the gaskets are _outside_ the current collector and separator - the only part that defines the thickness of the channel is the thickness of the cell channel spacer. This allows granular tuning of channel thickness by printing channels of varying thickness
    - This was intentionally done to more easily study electrode thickness which slurry electrodes are sensitive to. This also means channel thickness won't change with compression/torque.
- There is a third small hole in the electrolyte chamber - it was originally intended for gas sparging but may also be used for electrolyte recirculation in the electrolyte chamber. In the current version bubbles may occlude the reference/counter electrodes which can result in some noise. I included small holes at the top of the reference electrode port to allow for slightly better gas distribution. Your mileage may vary.
- Inside each "part type" folder, there may be multiple versions of a "part type". For example for "inlet" parts, there is a closed flow manifold if only the flowing electrolyte is of interest. If, for example, an electrode is under study, there is an additional "air electrode" inlet plate that includes an `8 mm x 20 mm` window open to the air, where the current collector can be replaced by an air electrode membrane electrode assembly.
- The flow channels have exposed surface areas of about `232 mm^2`. After accounting for the inlet port holes, the current collector surface area is `207 mm^2`. This will generally vary slightly with printer tolerance but most decent printers will get it within the square mm.To clarify:

<img width="547" height="587" alt="image" src="https://github.com/user-attachments/assets/58792d47-e4ab-4702-ae73-b3cc5e65b2a0" />


# Fine Print

## License Summary
CC BY-NC-SA 4.0
- **Attribution (BY)**: Please give appropriate credit.
- **Non-Commercial (NC)**: Usage is limited to research, educational, and personal applications.
- **Share-Alike (SA)**: Any derivatives must be shared under the same license.

## Allowed Uses
- Personal projects
- Educational or research purposes
- Non-commercial open-source projects
- Modifying and sharing designs under the same license

## Disallowed Uses
- Selling the files or any product derived from them
- Using the designs in a commercial project without explicit permission
- Removing attribution or license information
