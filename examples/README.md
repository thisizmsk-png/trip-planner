# Example output

[`lisbon-sintra-porto.pdf`](lisbon-sintra-porto.pdf) is a real, unedited run of this skill: a 5-day, two-base Portugal trip that flies into Lisbon and out of Porto, so it never backtracks.

It shows what the skill actually produces:

- **Geography first.** The plan relocates the base from Lisbon to Porto on day 3 instead of day-tripping Porto. A Lisbon round trip would be 6 to 7 hours of driving and the departure airport is on the wrong end.
- **A red-team baked into the deliverable.** The two alert cards name the load-bearing constraint (the Monday evening OPO flight, with many museums closed on that Monday) and the perishable bookings with all-in pricing.
- **Hours checked for the real dates.** Jeronimos Monastery and Belem Tower are closed Mondays, so they sit on day 1, not on the Monday departure.
- **25 tappable Google Maps links**, one per stop and one per drive leg, verified clickable in the PDF.

`lisbon-sintra-porto.html` is the source. Render it with headless Chrome:

```bash
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless --disable-gpu \
  --run-all-compositor-stages-before-draw --virtual-time-budget=3000 \
  --print-to-pdf="lisbon-sintra-porto.pdf" "file://$PWD/lisbon-sintra-porto.html"
```
