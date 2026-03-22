# User Workflow Journey: Parent Fund Management for Youth Account

## Experience Mindset
Parents have multiple experiences with youth accounts: onboarding, allocating funds, managing spending limits, monitoring activity, and troubleshooting issues. Each experience contains several scenarios, which we explore below.

---

## User & Business Goals
- **User Goal:** Empower parents to allocate funds, set limits, and monitor youth spending easily, securely, and transparently.
- **Business Goal:** Increase engagement by providing tools that foster financial literacy in youths while ensuring parental control, trust, and satisfaction.

---

# Scenarios & Workflow Design Variations

## Scenario 1: Parent Accesses Youth Account Dashboard
### Context: Parent is logged in and wants to view/manage youth account

### Variation 1: Direct Dashboard Access
- **Workflow:**
  1. Parent logs in → 2. Selects "Youth Account" from main navigation → 3. Arrives at Youth Account Dashboard
- **User Goal:** Quickly view youth account balance and recent activity
- **Business Goal:** Maximize dashboard discoverability and ease of use

### Variation 2: Dashboard via Notifications
- **Workflow:**
  1. Parent logs in → 2. Sees notification (e.g., "Youth account update") → 3. Clicks notification → 4. Arrives at Youth Account Dashboard
- **User Goal:** Respond to important updates efficiently
- **Business Goal:** Drive engagement through proactive alerts

#### Screens & Details
- **1.0 Youth Account Dashboard**
  - **Goal:** Provide overview of youth account status and actions
  - **Description:** Shows current balance, recent transactions, spending limit, and quick actions (Add Funds, Set Limit)
  - **Design Problems:**
    - HMW surface critical info without clutter?
    - HMW prioritize actions for first-time vs. returning users?
  - **Design Opportunities:**
    - What if dashboard adapts based on usage patterns?
    - What if a virtual assistant guides new users?

- **Er.1 Dashboard Load Failure**
  - **Goal:** Communicate technical issues clearly
  - **Description:** Error message with retry/help options
  - **Design Problems:**
    - HMW minimize anxiety during outages?
  - **Design Opportunities:**
    - What if there’s a direct support chat?

**Sequence:** 1.0 Youth Account Dashboard → [Er.1 if error]

---

## Scenario 2: Parent Allocates Funds to Youth Account
### Context: Parent wants to transfer money to youth account

### Variation 1: From Dashboard Quick Action
- **Workflow:**
  1. On dashboard, clicks "Add Funds" → 2. Enters amount, selects source account → 3. Reviews & confirms → 4. Sees success/failure message

### Variation 2: From Dedicated Fund Transfer Page
- **Workflow:**
  1. Navigates to "Manage Funds" → 2. Follows step-by-step wizard: Select source → Enter amount → Confirm → Success/Error

#### Screens & Details
- **2.0 Fund Transfer Modal/Page**
  - **Goal:** Enable seamless fund allocation
  - **Description:** Source account selector, amount input, transfer limits, confirmation step
  - **Design Problems:**
    - HMW prevent accidental transfers?
    - HMW clarify available balance?
  - **Design Opportunities:**
    - What if preset amounts are suggested?

- **Pu.1 Fund Transfer Confirmation**
  - **Goal:** Prevent mistakes before finalizing
  - **Description:** Summarizes transfer, requests confirmation

- **Pu.2 Success Message**
  - **Goal:** Reassure and inform next steps
  - **Description:** Shows updated balance, option to repeat

- **Er.2 Insufficient Balance Error**
  - **Goal:** Clearly communicate why transfer failed
  - **Description:** Error explaining insufficient funds, with suggestions (e.g., pick another account)

**Sequence:** 1.0 Dashboard → 2.0 Fund Transfer → Pu.1 Confirm → Pu.2 Success / Er.2 Error

---

## Scenario 3: Parent Sets/Manages Spending Limit
### Context: Parent wants to control youth’s weekly spending

### Variation 1: Inline Editing on Dashboard
- **Workflow:**
  1. On dashboard, sees current limit → 2. Clicks "Edit Limit" → 3. Updates value → 4. Saves

### Variation 2: Via Dedicated Limit Management Page
- **Workflow:**
  1. Navigates to "Manage Limits" → 2. Enters new value, reads guidance → 3. Saves

#### Screens & Details
- **3.0 Spending Limit Configuration**
  - **Goal:** Make setting limits simple and informative
  - **Description:** Input for weekly limit, display of current/previous limits, contextual help
  - **Design Problems:**
    - HMW prevent invalid/unsafe values?
    - HMW explain how limits work?
  - **Design Opportunities:**
    - What if parents see usage insights before setting limits?

- **Pu.3 Limit Saved Confirmation**
  - **Goal:** Confirm change and reinforce control
  - **Description:** Success message with new limit

- **Er.3 Invalid Limit Error**
  - **Goal:** Prevent and explain input errors
  - **Description:** Inline error for out-of-range/non-numeric values

**Sequence:** 1.0 Dashboard → 3.0 Limit Config → Pu.3 Confirmation / Er.3 Error

---

## Scenario 4: Parent Views Youth Spending Activity
### Context: Parent wants to monitor transactions

### Variation 1: Activity Preview on Dashboard
- **Workflow:**
  1. On dashboard, sees recent transactions list → 2. Clicks "View All" for full history

### Variation 2: Filtered Activity Page
- **Workflow:**
  1. Navigates to "Activity" tab/page → 2. Applies filters (date, type)

#### Screens & Details
- **4.0 Activity List**
  - **Goal:** Make transaction history scannable and actionable
  - **Description:** List with date, merchant, amount, remaining balance, filters by period/type
  - **Design Problems:**
    - HMW help parents spot unusual spending?
    - HMW support accessibility for long lists?
  - **Design Opportunities:**
    - What if system flags suspicious transactions?

**Sequence:** 1.0 Dashboard → 4.0 Activity List

---

## Scenario 5: Insufficient Balance Handling During Transfer
### Context: Parent tries to transfer more than available

### Variation 1: Inline Error on Amount Entry
- **Workflow:**
  1. Enters amount > balance → 2. Sees immediate error, can adjust

### Variation 2: Error Only on Confirmation
- **Workflow:**
  1. Enters amount, proceeds to confirmation → 2. System checks, blocks, and shows error

#### Screens & Details
- **Er.2 Insufficient Balance Error** (see above)

**Sequence:** 2.0 Fund Transfer → Er.2 Error

---

# Screen Sequence Summaries (by Scenario & Variation)

## 1. Dashboard Access
- Variation 1: 1.0 Dashboard
- Variation 2: Notification → 1.0 Dashboard

## 2. Fund Allocation
- Variation 1: 1.0 Dashboard → 2.0 Fund Transfer → Pu.1 Confirm → Pu.2 Success / Er.2 Error
- Variation 2: 1.0 Dashboard → Manage Funds → 2.0 Fund Transfer → Pu.1 Confirm → Pu.2 Success / Er.2 Error

## 3. Spending Limit
- Variation 1: 1.0 Dashboard → 3.0 Limit Config → Pu.3 Confirmation / Er.3 Error
- Variation 2: 1.0 Dashboard → Manage Limits → 3.0 Limit Config → Pu.3 Confirmation / Er.3 Error

## 4. Activity Monitoring
- Variation 1: 1.0 Dashboard → 4.0 Activity List
- Variation 2: 1.0 Dashboard → Activity Tab → 4.0 Activity List (with filters)

## 5. Error Handling
- Inline or confirmation error states as above

---

# Minimum Viable Experience (MVE)
- **Scenario:** Parent logs in, views dashboard, adds funds, sets spending limit, checks activity, and handles errors.
- **Screens:** 1.0 Dashboard, 2.0 Fund Transfer, 3.0 Limit Config, 4.0 Activity List, Pu.1/Pu.2/Pu.3 confirmations, Er.1/Er.2/Er.3 errors

---

# Accessibility & Scalability Notes
- All screens must meet WCAG 2.1 AA: keyboard navigation, screen reader labels, color contrast
- Flows support expansion (multiple youth accounts, additional controls, etc.)
- Responsive layouts for desktop, tablet, mobile

---

# Edge Cases & Use Cases
- Parent with multiple youth accounts: dashboard adapts to show all
- Attempt to transfer with insufficient funds: clear error, alternate options
- Invalid spending limit: error and guidance
- Large transaction history: filters, pagination, accessibility
- Technical errors: support, retry, and fallback flows

---

# Summary Table of Screens
| Screen ID | Title                        | Purpose/Goal                               |
|-----------|-----------------------------|--------------------------------------------|
| 1.0       | Youth Account Dashboard     | Overview, quick actions                    |
| 2.0       | Fund Transfer               | Allocate funds to youth account            |
| 3.0       | Spending Limit Config       | Set/manage weekly spending limits          |
| 4.0       | Activity List               | View/filter youth spending history         |
| Pu.1      | Fund Transfer Confirmation  | Confirm allocation before commit           |
| Pu.2      | Success Message             | Confirm completion of action               |
| Pu.3      | Limit Saved Confirmation    | Confirm limit update                       |
| Er.1      | Dashboard Load Failure      | Handle technical errors                    |
| Er.2      | Insufficient Balance Error  | Handle failed fund allocation              |
| Er.3      | Invalid Limit Error         | Handle invalid input for limits            |

---

# End of Workflow Documentation
