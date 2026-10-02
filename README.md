# East Frisia Storm Explorer

An interactive page that shows how a storm changes the sea bed around the East Frisian islands (German North Sea coast).

**Open it here:** https://vince-mmy.github.io/Storm-exporer/

It runs entirely in the browser. There is nothing to install and no login.

## What it shows

The bed level change over a 72-hour storm in four areas: Norderney, Langeoog and two ebb-tidal deltas (Delta JN and Delta NBL). Results are 45 m block means.

## How to use it

1. Pick a storm from the list (for example Xaver 2013), or set your own with the four sliders: peak wave height, hours with waves above 3 m, peak water level and wave direction.
2. The map shows erosion and deposition. The sketch under the sliders shows the storm you chose.
3. The table gives erosion and deposition volumes per area.
4. Press "New section" and click on the map to draw a line. The page plots the bed change along it and lets you copy the values as CSV.

## Where the numbers come from

The maps come from a machine-learning emulator (gradient-boosted trees) trained on XBeach storm simulations. They are not XBeach results themselves.

## Limits

- On storms the model has not seen, the erosion volume is off by about 10 % (median), and the pattern correlates with XBeach at r ≈ 0.9.
- The model cannot extrapolate. Outside the range of the training storms it returns the result of the nearest training values, and the page shows a warning.
- Storms with more than 57 hours of waves above 3 m get too little erosion.
- Results exist only inside the four areas. Bed above +3 m NHN (dunes, islands) is not modelled.
- Changing the storm mostly changes the size of the response. The pattern is set mainly by the bed.

## Files

- `index.html` is the whole application: page, model and data in one file.

## Contact

Developer: Mengyao Ma, mengyao.ma@hereon.de
