# Statement of Work: Excerpt

**Client:** Pinewick Industrial Supply (fictional training material)
**Program:** Service & Returns
**Prepared by:** Saltbox
**Status:** Signed

> This excerpt contains the scope sections relevant to the delivery team. Commercial terms, rates, and schedule are omitted.

## 1. Background

Pinewick Industrial Supply operates a Salesforce B2B Commerce (LWR) storefront with Salesforce Order Management, live for approximately eighteen months, serving roughly 9,000 business accounts across twelve branches and three distribution centers. Service Cloud is in use for email-to-case. Returns, credits, and warranty claims are handled manually by branch staff through the ERP and email, and account for approximately one quarter of support contacts.

## 2. Objectives

1. Allow account buyers to initiate and track product returns and warranty claims from the storefront without contacting a branch.
2. Apply Pinewick's return eligibility and restocking-fee policy consistently across all branches and accounts.
3. Reduce return- and warranty-related support contacts by at least 50% within six months of go-live.
4. Give branch and order-operations staff a single view of open returns and claims in Salesforce.

## 3. Scope

### 3.1 Epic: Returns & Warranty Claims

- A buyer can start a return from an order in storefront order history, selecting lines and quantities.
- Eligibility is evaluated per line against Pinewick's policy (return window, non-returnable categories, order type) and the result shown to the buyer before submission.
- The applicable restocking fee is calculated and displayed before submission, honoring account-level contractual terms.
- An approved return obtains an RMA number from the ERP and presents the buyer with a carrier return label or branch drop-off instructions, per line category.
- Return status (requested, RMA issued, in transit, received, credited) is visible to the buyer in the storefront and to staff in Salesforce.
- A buyer can submit a warranty claim for an eligible product, and the claim is transmitted to the manufacturer with the information the manufacturer requires.
- Staff can view, approve, and manage returns and claims in Service Cloud.

### 3.2 Epic: Order Support Cases

- Buyers can raise order-status and invoice cases from the storefront; cases route to the owning branch.

### 3.3 Epic: Account Self-Service

- Account administrators can manage buyer users, ship-to addresses, and view payment terms.

## 4. Out of scope

- Changes to the ERP's returns, receiving, or credit-memo processes beyond consuming its existing APIs.
- Inter-branch inventory transfers or stock adjustments.
- Manufacturer warranty portal integrations beyond a structured submission (email or file) per manufacturer.
- Custom reporting or dashboards beyond standard Salesforce reports on the objects delivered.
- Printed or custom-branded shipping documentation beyond the carrier's standard label.
- Any change to storefront checkout, pricing, or payment terms.

## 5. Integrations in scope

| System | Direction | Purpose |
|---|---|---|
| ERP | Salesforce → ERP → Salesforce | RMA creation; return receipt and credit-memo status |
| Carrier label service | Salesforce → carrier | Return shipping labels |
| Manufacturer warranty process | Salesforce → manufacturer | Structured claim submission |

## 6. Assumptions

- The ERP exposes an RMA-creation API and a return/credit-status query; Pinewick IT owns the ERP relationship and any changes on that side.
- Pinewick provides the current return policy, restocking-fee rules, and non-returnable category list in writing during Align.
- Pinewick provides sandbox environments matching production configuration.
- Pinewick supplies testers for user acceptance testing from returns, branch operations, and at least one buyer account.

## 7. Delivery approach

Saltbox Success System: Align, Prototype Review, Build (three-week iterations), Test & Launch with hypercare. Prototype Review confirms effort and iteration count before Build begins.