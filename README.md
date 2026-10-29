# Shivalingeshwara Arts Material Price Estimator

A small offline-friendly price estimator built with plain HTML, CSS, and JavaScript. No npm, build process, framework, backend, or database is required.

## Run it

1. Extract the folder.
2. Open `index.html` in Chrome, Edge, or another modern browser.
3. Choose **Edit prices & settings** to update the starter material prices and the machine electricity assumptions.
4. Use **Export backup** occasionally to save your custom settings as a JSON file.

## How the estimate is calculated

- Billable area = width (ft) × height (ft) × quantity.
- Material cost = billable area × material rate per sq.ft.
- Design, labour/making, and maintenance/wastage are each calculated as a percentage of material cost.
- Machine electricity = machine time in minutes ÷ 60 × units/hour × electricity rate per unit.
- Final estimate = material cost + the three percentage additions + machine electricity.

The three percentage fields start at 0% intentionally. Set them to your own pricing policy. The percentages are additive and are not compounded.

## About the starter values

Starter values were taken from online Indian listings searched on 29 October 2026. They are not supplier quotations for Haveri, and the cited suppliers do not all sell the same grade or thickness. Some values are calculated from a listed piece price and its stated size; some are estimates where no exact thickness or finish could be matched. Replace these with your invoice rates before using the app for customer quotations.

Key sources are linked inside the **Edit prices & settings** tab under each row and under **Price sources used**. Online asking prices may exclude GST, transport, and minimum-order conditions.

## Machine assumptions from your earlier information

- Estimated laser consumption: 2 kWh per running hour (user-reported estimate; not verified with a power meter).
- Electricity rate: ₹10/unit as an editable working assumption.
- Machine usage: around 20 hours/month or less.
- Total monthly power bill: about ₹1,000 including other loads. PC use was described as around 10 hours/day and a fan around 8 hours/day.

The app estimates laser electricity per job from the runtime minutes you enter. It does not automatically allocate the entire monthly electricity bill to a job, because the PC/fan wattage and actual productive output are unknown.

## Data storage

Prices and settings are saved with browser `localStorage` on the current device. There is no cloud sync. If browser site data is cleared or you use a different browser/device, your saved values may not be available; use **Export backup** to keep a copy.
