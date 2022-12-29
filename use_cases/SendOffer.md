# Use-Case Specification: Send offer

## 1. Brief Description
If an offer meets the seller's configured requirements it will mark the item as sold even if the seller has not manually accepted it. This is useful for getting ahead of other sellers on popular items by sticking closely to the listed price. If the requirement is not met the seller may accept, reject or counter the offer based on the buyers reasoning.

## 2. Mockup
![Send offer](/mockups/Checkout.png)

## 3. Activity Diagrams
With seller side configuration:\
![Activity Diagram](/resources/activity_diagrams/ActivityDiagramSendOfferAutoAccept.png)

Without configuration:\
![Activity Diagram](/resources/activity_diagrams/ActivityDiagramSendOffer.png)

## 4. Preconditions
- Sender and recipient exist
- Item has not been sold yet

## 4. Postconditions
- If the bid is high enough it is accepted