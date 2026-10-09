# Project Case Study — Back Office Operations & MIS

## Business problem
Small operations teams need accurate stock visibility, traceable inventory movements, purchase-order status, timely reorder alerts and a compact weekly report. Manual entries without validation can hide shortages or create mismatches.

## Solution built
- Inventory register with 20 synthetic SKUs across five categories.
- Formula-driven quantity moved, current stock, stock value and reorder flag.
- Stock movement ledger with signed quantities: receipts positive, issues negative.
- Purchase-order tracker with ordered, received and outstanding quantities plus status.
- Dashboard with SKU count, stock value, reorder alerts, open POs and category summary.
- Weekly MIS by category.
- Three SOPs covering goods receiving, stock issue/dispatch and daily record verification.

## Example formulas / logic
- Quantity change per SKU = sum of signed ledger movements for that SKU.
- Current stock = opening stock + quantity change.
- Stock value = current stock × unit cost.
- Reorder alert = current stock less than or equal to reorder point.
- PO outstanding quantity = max(0, ordered quantity − received quantity).
- PO status = Received, Open or Part received according to the quantities entered.

## Tools and skills demonstrated
Excel formulas (`SUMIF`, `COUNTIF`, `IF`, `MAX`), dropdown validation, conditional formatting, charting, inventory control, purchase-order tracking, reconciliation and SOP writing.

## Data and limitations
All items, suppliers, quantities and order references are fictional. The workbook is a practice model, not a live inventory system. Weekly issued quantities are calculated by category from stock-ledger rows marked Issue, using the recorded signed quantity.

## Possible next iteration
Add a formal adjustment approval log, a stock-count variance sheet and a monthly trend report. Only use real records in an access-controlled employer environment.
