# Document 1: User Requirements Specification (URS)
**Project:** Grill & Go Digital Ordering & Fulfillment System  
**Client:** Uncle Bob (Grill & Go, Orchard Road)  
**Module:** Software Engineering  

---

## 1. Agile User Stories & BDD Acceptance Criteria

### US-01: Table QR Code Menu Access & Customization (Customer)
* **As a** Customer sitting at a table,
* **I want to** scan a table-specific QR code to view the menu on my mobile browser[cite: 1],
* **So that** I can customize my order (steak doneness, side dishes) without downloading an app or waiting in line[cite: 1].

**Acceptance Criteria (Given-When-Then):**
* **Given** I am seated at Table 5 and scan the table QR code on my mobile phone[cite: 1],
* **When** the web menu loads[cite: 1],
* **Then** I should see the full menu with customization options (e.g., Medium Rare, Mashed Potato)[cite: 1].

---

### US-02: Immediate Digital Payment (Customer)
* **As a** Customer[cite: 1],
* **I want to** pay immediately via PayNow QR or Credit Card prior to order submission[cite: 1],
* **So that** my payment is confirmed instantly and sent directly to the kitchen[cite: 1].

**Acceptance Criteria (Given-When-Then):**
* **Given** I have items in my digital cart[cite: 1],
* **When** I proceed to checkout and select "PayNow QR"[cite: 1],
* **Then** a dynamic PayNow QR code is displayed, and upon payment, my order is sent to the kitchen display system[cite: 1].

---

### US-03: Real-Time Order Display on Kitchen Tablet (Kitchen Staff)
* **As a** Kitchen Staff member[cite: 1],
* **I want to** view incoming paid orders in real time on the Kitchen Display System (KDS) tablet[cite: 1],
* **So that** our team can prepare meals accurately in the order they were received[cite: 1].

**Acceptance Criteria (Given-When-Then):**
* **Given** a customer completes payment for an order[cite: 1],
* **When** the payment is verified by the backend[cite: 1],
* **Then** the order appears instantly on the KDS tablet screen with item details and table number[cite: 1].

---

### US-04: Kitchen Order Status Updates (Kitchen Staff)
* **As a** Kitchen Staff member[cite: 1],
* **I want to** update the status of an order (`Pending` → `Preparing` → `Ready for Pickup`)[cite: 1],
* **So that** customers know when their meal is ready for collection[cite: 1].

**Acceptance Criteria (Given-When-Then):**
* **Given** an order is currently in `Preparing` status[cite: 1],
* **When** I tap `Mark as Ready` on the KDS tablet[cite: 1],
* **Then** the order status updates to `Ready for Pickup` and notifies the customer display screen[cite: 1].

---

### US-05: Real-Time Menu Item Override (Store Manager)
* **As a** Store Manager[cite: 1],
* **I want to** toggle menu items as "Out of Stock" in real time[cite: 1],
* **So that** customers cannot place orders for items that have run out[cite: 1].

**Acceptance Criteria (Given-When-Then):**
* **Given** the stall has run out of Sirloin Steak[cite: 1],
* **When** I toggle "Sirloin Steak" to "Out of Stock" on the manager interface[cite: 1],
* **Then** the item immediately displays as "Sold Out" on all customer mobile browser menus[cite: 1].

---

### US-06: Off-the-Shelf BI Tool Sales Analytics (Store Manager / Owner)
* **As** Uncle Bob (Owner)[cite: 1],
* **I want to** connect Power BI or Tableau directly to the transactional database[cite: 1],
* **So that** I can analyze peak-hour sales trends and revenue without custom reporting modules[cite: 1].

**Acceptance Criteria (Given-When-Then):**
* **Given** sales data stored in the relational database[cite: 1],
* **When** Power BI connects to the transactional database via standard SQL drivers[cite: 1],
* **Then** dynamic dashboards display peak order hours and total monthly sales[cite: 1].

---

## 2. UML Use Case Diagram

```mermaid

Delete everything **inside that Mermaid block**.

Replace it with this:

```mermaid
flowchart LR

    Customer["Customer"]
    KitchenStaff["Kitchen Staff"]
    Manager["Store Manager"]
    PayNow["PayNow Gateway"]
    BI["Power BI / Tableau"]

    subgraph System["Grill & Go System"]
        UC1(["Browse Menu & Customize Order"])
        UC2(["Place Order"])
        UC3(["Make Payment"])
        UC4(["View Incoming Orders (KDS)"])
        UC5(["Update Order Status"])
        UC6(["Toggle Menu Item Availability"])
        UC7(["Generate Sales & Revenue Reports"])
    end

    Customer --> UC1
    Customer --> UC2

    UC2 -. "<<include>>" .-> UC3
    UC3 --> PayNow

    KitchenStaff --> UC4
    KitchenStaff --> UC5

    Manager --> UC6
    Manager --> UC7

    BI --> UC7

at the end.

So the complete section should look like:

```markdown
## 2. UML Use Case Diagram

```mermaid
flowchart LR

    Customer["Customer"]
    KitchenStaff["Kitchen Staff"]
    Manager["Store Manager"]
    PayNow["PayNow Gateway"]
    BI["Power BI / Tableau"]

    subgraph System["Grill & Go System"]
        UC1(["Browse Menu & Customize Order"])
        UC2(["Place Order"])
        UC3(["Make Payment"])
        UC4(["View Incoming Orders (KDS)"])
        UC5(["Update Order Status"])
        UC6(["Toggle Menu Item Availability"])
        UC7(["Generate Sales & Revenue Reports"])
    end

    Customer --> UC1
    Customer --> UC2

    UC2 -. "<<include>>" .-> UC3
    UC3 --> PayNow

    KitchenStaff --> UC4
    KitchenStaff --> UC5

    Manager --> UC6
    Manager --> UC7

    BI --> UC7

---

## Step 3 — Commit the change

After replacing it, scroll down and click:

**Commit changes**

For the commit message, use:

```text
Fix UML use case diagram rendering

    
