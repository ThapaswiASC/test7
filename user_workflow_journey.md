# UX Workflow Documentation: Parent Management of Youth Account Funds

## Experience Overview
Parents can allocate and manage funds for a youth account, set spending limits, and monitor youth spending activity. The experience must be intuitive, accessible, and scalable to support diverse family structures and future product enhancements.

---

## Key User Scenarios & Variations

### Scenario 1: Access Youth Account Dashboard
**Context:** Parent is logged in and wants to check youth account status and activity.

#### Variation A: Direct Navigation
- **Workflow:**
  1. Parent logs in
  2. Selects 'Youth Accounts' from main dashboard
  3. Youth account dashboard loads, showing balance, recent activity, quick actions

#### Variation B: Notification-Driven Entry
- **Workflow:**
  1. Parent receives notification (e.g., youth made a transaction)
  2. Clicks notification, which deep-links to youth account dashboard

**User Goal:** Quickly view youth account status and recent activity.
**Business Goal:** Promote parental engagement and trust.

**Screens:**
- **1.0 Parent Main Dashboard**
  - **Goal:** Entry point to all parent features
  - **Description:** Shows all accounts, notifications, and navigation
  - **Design Problems:** HMW make youth account entry prominent but not overwhelming?
  - **Opportunities:** What if dashboard adapts to show youth account summary if recent activity?

- **2.0 Youth Account Dashboard**
  - **Goal:** Central hub for youth account management
  - **Description:** Balance, recent transactions, quick actions (Add Funds, Set Limit)
  - **Design Problems:** HMW communicate key info at-a-glance?
  - **Opportunities:** What if dashboard highlights unusual spending or achievements?

- **Sequence:** 1.0 Parent Main Dashboard → 2.0 Youth Account Dashboard

---

### Scenario 2: Allocate Funds to Youth Account
**Context:** Parent wants to add funds to youth account.

#### Variation A: Modal-Based Transfer
- **Workflow:**
  1. On youth account dashboard, parent clicks 'Add Funds'
  2. Modal opens for transfer details (source, amount)
  3. Parent confirms transfer
  4. Success/failure message shown

#### Variation B: Dedicated Transfer Page
- **Workflow:**
  1. From dashboard, parent clicks 'Add Funds'
  2. Redirected to full transfer page for details and confirmation
  3. Success/failure message shown

**User Goal:** Easily transfer funds to youth account.
**Business Goal:** Encourage regular funding and reinforce financial education.

**Screens:**
- **2.1 Add Funds Modal/Page**
  - **Goal:** Simple, clear fund transfer
  - **Description:** Source account, amount, validation, confirm
  - **Design Problems:** HMW prevent errors and accidental transfers?
  - **Opportunities:** What if we suggest amounts based on spending patterns?

- **Pu.1 Success/Failure Pop-Up**
  - **Goal:** Immediate feedback on transfer
  - **Description:** Success or error message (e.g., insufficient funds)
  - **Design Problems:** HMW make errors actionable?
  - **Opportunities:** What if we offer tips on recurring transfers?

- **Er.1 Insufficient Balance Error**
  - **Goal:** Prevent failed transactions
  - **Description:** Clear error with guidance to resolve
  - **Design Problems:** HMW reduce frustration from errors?
  - **Opportunities:** What if we offer alternate funding options?

- **Sequence (A):** 2.0 Youth Account Dashboard → 2.1 Add Funds Modal → Pu.1 Success/Failure
- **Sequence (B):** 2.0 Youth Account Dashboard → 2.1 Add Funds Page → Pu.1 Success/Failure

---

### Scenario 3: Set Spending Limit
**Context:** Parent wants to set or edit weekly spending limit for youth.

#### Variation A: Inline Editing on Dashboard
- **Workflow:**
  1. On dashboard, parent sees current limit
  2. Clicks 'Edit', enters new value inline
  3. Confirmation prompt
  4. Limit updated and displayed

#### Variation B: Guided Configuration Page
- **Workflow:**
  1. Parent clicks 'Manage Limit' (dashboard)
  2. Taken to dedicated page with guidance and examples
  3. Enters/edits limit, confirms
  4. Returns to dashboard with updated limit

**User Goal:** Set/adjust spending limit confidently and easily.
**Business Goal:** Empower parents to teach budgeting and control.

**Screens:**
- **2.2 Spending Limit Display/Editor**
  - **Goal:** Fast access to limit controls
  - **Description:** Shows active limit, edit option, validation
  - **Design Problems:** HMW explain limits without jargon?
  - **Opportunities:** What if we show projected savings based on limit?

- **Pu.2 Edit Confirmation**
  - **Goal:** Prevent mistakes in limit setting
  - **Description:** Confirm before saving new value
  - **Design Problems:** HMW reduce accidental edits?
  - **Opportunities:** What if we show comparison to average limits?

- **Sequence (A):** 2.0 Youth Account Dashboard → 2.2 Inline Editor → Pu.2 Confirmation
- **Sequence (B):** 2.0 Youth Account Dashboard → 2.2 Configuration Page → Pu.2 Confirmation

---

### Scenario 4: View Youth Spending Activity
**Context:** Parent wants to review youth’s transactions.

#### Variation A: List with Filters
- **Workflow:**
  1. On dashboard, parent clicks 'View Activity'
  2. Transaction list loads with time filters

#### Variation B: Visual Insights View
- **Workflow:**
  1. Parent clicks 'View Activity'
  2. Transaction list loads with summary graphs (e.g., category spend)

**User Goal:** Understand youth’s spending patterns.
**Business Goal:** Increase transparency and foster financial conversations.

**Screens:**
- **2.3 Activity List**
  - **Goal:** Scan and filter transactions
  - **Description:** List with date, merchant, amount, remaining balance, filters
  - **Design Problems:** HMW make patterns obvious?
  - **Opportunities:** What if we flag unusual activity or trends?

- **2.4 Activity Insights**
  - **Goal:** Visualize spending
  - **Description:** Graphs for categories, time trends
  - **Design Problems:** HMW avoid overwhelming with data?
  - **Opportunities:** What if we suggest conversation starters for parents?

- **Sequence (A):** 2.0 Youth Account Dashboard → 2.3 Activity List
- **Sequence (B):** 2.0 Youth Account Dashboard → 2.4 Activity Insights

---

### Scenario 5: Handle Insufficient Balance During Fund Allocation
**Context:** Parent tries to transfer more than available in their account.

#### Variation A: Pre-Transfer Validation
- **Workflow:**
  1. Parent enters amount
  2. System checks balance before confirmation
  3. Error message if insufficient

#### Variation B: Post-Confirmation Error
- **Workflow:**
  1. Parent enters amount, confirms
  2. System attempts transfer, error if insufficient

**User Goal:** Understand why a transfer fails and how to resolve it.
**Business Goal:** Reduce failed transactions, increase satisfaction.

**Screens:**
- **Er.1 Insufficient Balance Error (reused)**
  - **Goal:** Prevent confusion, guide resolution
  - **Description:** Clear, actionable error with suggestions
  - **Design Problems:** HMW avoid repeat errors?
  - **Opportunities:** What if we offer to set a reminder when funds are available?

- **Sequence (A):** 2.1 Add Funds Modal → Er.1 Insufficient Balance Error
- **Sequence (B):** 2.1 Add Funds Modal → Pu.1 Success/Failure

---

## Minimum Viable Experience (MVE)
**Scenario:** Parent allocates funds, sets spending limit, and reviews activity for youth account.
- **User Goal:** Empower parents to manage youth funds efficiently.
- **Business Goal:** Foster trust, engagement, and financial literacy.
- **Screens:**
  1.0 Parent Main Dashboard
  2.0 Youth Account Dashboard
  2.1 Add Funds Modal/Page
  2.2 Spending Limit Editor
  2.3 Activity List
  Pu.1 Success/Failure Pop-Up
  Pu.2 Limit Edit Confirmation
  Er.1 Insufficient Balance Error

**Sequence:** 1.0 → 2.0 → 2.1/2.2/2.3 → Pu.1/Pu.2/Er.1 as needed

---

## Accessibility & Scalability Notes
- All flows support keyboard navigation and screen readers
- Color contrast and font sizes meet WCAG 2.1 AA
- Flows designed for future extension (e.g., multiple youth accounts, additional controls)
- Responsive layouts for desktop, tablet, and mobile

---

## Summary Table of Screens & Flows
| Screen ID | Title                       | Goal                                 | Key Design Problems                    | Opportunities                         |
|-----------|-----------------------------|--------------------------------------|----------------------------------------|----------------------------------------|
| 1.0       | Parent Main Dashboard       | Entry point, navigation              | HMW highlight youth features?          | Adaptive dashboard                     |
| 2.0       | Youth Account Dashboard     | Manage youth funds                   | HMW organize info at-a-glance?         | Highlight achievements, alerts         |
| 2.1       | Add Funds Modal/Page        | Transfer funds                       | HMW prevent errors?                    | Suggest recurring transfers            |
| 2.2       | Spending Limit Editor       | Set/edit weekly limit                | HMW explain limits?                    | Show projected savings                 |
| 2.3       | Activity List               | Review transactions                  | HMW show patterns?                     | Flag trends, suggest conversations     |
| 2.4       | Activity Insights           | Visualize spending                   | HMW avoid data overload?               | Personalized insights                  |
| Pu.1      | Success/Failure Pop-Up      | Confirm result                       | HMW make errors actionable?            | Offer solutions                        |
| Pu.2      | Limit Edit Confirmation     | Prevent mistakes                     | HMW reduce accidental edits?           | Show comparisons                       |
| Er.1      | Insufficient Balance Error  | Resolve failed transfers             | HMW reduce frustration?                | Set reminders, offer guidance          |

---

## End-to-End Flow (Example)
1. Parent logs in → 1.0
2. Selects Youth Account → 2.0
3. Adds funds → 2.1 → Pu.1/Er.1
4. Sets spending limit → 2.2 → Pu.2
5. Reviews activity → 2.3/2.4

---

## Edge Cases & Additional Scenarios
- Multiple youth accounts: Dashboard supports account switcher
- Parent with limited access: Some actions may be view-only
- Youth account locked/frozen: Dashboard shows status and guidance
- Accessibility: All actions possible via keyboard, ARIA labels present
- Mobile: All flows adapt to small screens

---

## Conclusion
These workflows ensure parents can confidently and efficiently manage youth accounts, balancing user needs for control and insight with business goals of engagement, education, and trust. Accessibility and scalability are core to all designs.
