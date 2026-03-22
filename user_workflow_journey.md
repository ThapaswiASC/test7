# UX Workflow Documentation: Parent Managing Youth Account

## Experience Mindset

**Primary User:** Parent/Guardian

**Experience:** Allocating and managing funds for a youth account to teach financial responsibility with oversight and control.

**Scenarios Identified:**
1. Accessing the Youth Account Dashboard
2. Allocating Funds to Youth Account
3. Setting Spending Limit
4. Viewing Youth Spending Activity
5. Handling Insufficient Balance during Fund Allocation

---

## 1. Accessing the Youth Account Dashboard

### Scenario A: Direct Navigation
- **Context:** Parent logs in and selects 'Youth Accounts' from main navigation.
- **Action:** System displays dashboard with current balance and recent activity.
- **Actor:** Parent
- **Goal:** Quickly access youth account overview.

### Scenario B: Notification-Driven Access
- **Context:** Parent receives notification about youth account activity and clicks link.
- **Action:** System deep-links to the youth account dashboard, highlighting recent activity.
- **Actor:** Parent
- **Goal:** Respond to activity or alert efficiently.

#### User Goal
- To easily and securely access an overview of the youth account, including balance and recent transactions.

#### Business Goal
- To ensure parents can monitor and manage youth accounts, increasing engagement and trust in digital banking tools.

#### Screens

##### 1.0 Youth Account Dashboard
- **Page Goal:** Provide a clear, actionable overview of youth account status.
- **Screen Description:**
  - Shows youth's name/profile, current balance, recent transactions, spending limit status, quick actions (Add Funds, Set Limit), and notifications/alerts.
- **Design Problems:**
  - HMW ensure parents understand all account features at a glance?
  - HMW prioritize urgent or important notifications without overwhelming?
- **Design Opportunities:**
  - What if the dashboard adapts to show the most relevant actions or alerts?
  - What if there is contextual guidance for new users?

##### 1.1 Dashboard - Notification Highlight State
- **Page Goal:** Draw attention to new or important activity.
- **Screen Description:**
  - Recent activity highlighted, with call-to-action if required (e.g., approve/reject transaction).
- **Design Problems:**
  - HMW avoid alert fatigue?
- **Design Opportunities:**
  - What if parents can customize notification preferences?

##### Er.1 Dashboard Load Error
- **Page Goal:** Communicate issues loading data and provide recovery options.
- **Screen Description:**
  - Error message, retry option, help link.
- **Design Problems:**
  - HMW reduce anxiety during technical issues?

#### Sequence: 1.0 -> 1.1 (if notification) / Er.1 (if error)

---

## 2. Allocating Funds to Youth Account

### Scenario A: Standard Transfer
- **Context:** Parent selects 'Add Funds' on dashboard.
- **Action:** Guided through selecting source account, entering amount, confirming transfer.
- **Actor:** Parent
- **Goal:** Transfer funds efficiently and securely.

### Scenario B: Quick Transfer (Preset Amounts)
- **Context:** Parent uses quick-action to transfer preset amounts ($10, $20, $50).
- **Action:** Minimal steps, confirmation only.
- **Actor:** Parent
- **Goal:** Rapidly add funds for routine needs.

#### User Goal
- To move money into the youth account with minimal friction and maximum clarity.

#### Business Goal
- Increase usage of youth accounts and reinforce parental control features.

#### Screens

##### 2.0 Fund Transfer Initiation
- **Page Goal:** Start the transfer process clearly.
- **Screen Description:**
  - Source account selector, amount input, preset options, estimated balance post-transfer.
- **Design Problems:**
  - HMW prevent accidental transfers?
- **Design Opportunities:**
  - What if the system suggests amounts based on past behavior?

##### 2.1 Transfer Confirmation
- **Page Goal:** Confirm details before committing transfer.
- **Screen Description:**
  - Summary of transfer, editable fields, confirm/cancel buttons.
- **Design Problems:**
  - HMW reduce errors at this critical step?

##### 2.2 Transfer Success
- **Page Goal:** Reassure and inform parent of successful transfer.
- **Screen Description:**
  - Success message, updated balance, option to set spending limit or view activity.
- **Design Problems:**
  - HMW encourage next logical actions?

##### Pu.1 Quick Transfer Pop-up
- **Page Goal:** Enable fast fund allocation.
- **Screen Description:**
  - Preset amount buttons, confirmation.
- **Design Problems:**
  - HMW support rapid yet secure actions?

##### Er.2 Insufficient Balance Error
- **Page Goal:** Clearly communicate why transfer failed.
- **Screen Description:**
  - Error message, suggestions (e.g., select different source, lower amount), help link.
- **Design Problems:**
  - HMW avoid frustration and support resolution?

#### Sequence: 2.0 -> 2.1 -> 2.2 / Er.2 (if insufficient funds)
- Alternate: Pu.1 (quick transfer) -> 2.2 / Er.2

---

## 3. Setting Spending Limit

### Scenario A: Manual Entry
- **Context:** Parent selects 'Set Spending Limit' and enters weekly limit.
- **Action:** Input value, confirm, see updated limit.
- **Actor:** Parent
- **Goal:** Restrict youth spending to a custom value.

### Scenario B: Guided Recommendation
- **Context:** System suggests a limit based on youth's age or past spending; parent accepts or edits.
- **Action:** Review, adjust, confirm.
- **Actor:** Parent
- **Goal:** Set appropriate limits with guidance.

#### User Goal
- To easily set and adjust spending limits to teach budgeting.

#### Business Goal
- Support financial literacy and parental peace of mind.

#### Screens

##### 3.0 Spending Limit Configuration
- **Page Goal:** Configure and understand spending limits.
- **Screen Description:**
  - Input for weekly limit, guidance text, display of current/previous limits, error handling for invalid values.
- **Design Problems:**
  - HMW make limits understandable for all users?
- **Design Opportunities:**
  - What if system explains benefits of setting limits?

##### 3.1 Limit Confirmation
- **Page Goal:** Confirm new limit.
- **Screen Description:**
  - Summary, confirm/cancel, effective date display.
- **Design Problems:**
  - HMW clarify when limits take effect?

##### 3.2 Limit Set Success
- **Page Goal:** Inform parent of active limit.
- **Screen Description:**
  - Success message, option to adjust or view youth activity.
- **Design Problems:**
  - HMW encourage ongoing engagement?

##### Pu.2 Guided Limit Recommendation
- **Page Goal:** Suggest appropriate limits.
- **Screen Description:**
  - Pre-filled suggestions, rationale, accept/edit.
- **Design Problems:**
  - HMW personalize guidance?

##### Er.3 Invalid Limit Entry
- **Page Goal:** Prevent and explain entry errors.
- **Screen Description:**
  - Inline error, help link.
- **Design Problems:**
  - HMW reduce confusion?

#### Sequence: 3.0 -> 3.1 -> 3.2 / Er.3
- Alternate: Pu.2 (guided) -> 3.1 -> 3.2

---

## 4. Viewing Youth Spending Activity

### Scenario A: Transaction List
- **Context:** Parent selects 'View Activity' from dashboard.
- **Action:** Sees transaction list with filters.
- **Actor:** Parent
- **Goal:** Monitor spending patterns and details.

### Scenario B: Filtered/Segmented View
- **Context:** Parent filters by date, amount, or merchant.
- **Action:** Sees only relevant transactions.
- **Actor:** Parent
- **Goal:** Focus on specific behaviors or time periods.

#### User Goal
- To quickly scan and understand how the youth is using their account.

#### Business Goal
- Reinforce transparency and trust in youth banking tools.

#### Screens

##### 4.0 Activity List
- **Page Goal:** Make all transactions visible and scannable.
- **Screen Description:**
  - List with date, merchant, amount, remaining balance, filters for period/type.
- **Design Problems:**
  - HMW support rapid pattern recognition?
- **Design Opportunities:**
  - What if system highlights unusual activity?

##### 4.1 Filtered Results
- **Page Goal:** Enable focused review.
- **Screen Description:**
  - Active filters, filtered transaction list.
- **Design Problems:**
  - HMW make filtering intuitive?

##### Er.4 No Transactions State
- **Page Goal:** Inform when no activity is present.
- **Screen Description:**
  - Friendly message, tips for first use.
- **Design Problems:**
  - HMW set expectations for new accounts?

#### Sequence: 4.0 -> 4.1 (if filtered) / Er.4 (if no data)

---

## 5. Handling Insufficient Balance during Fund Allocation

### Scenario A: Standard Error Handling
- **Context:** Parent tries to transfer more than available in source account.
- **Action:** System blocks transfer, shows error, suggests alternatives.
- **Actor:** Parent
- **Goal:** Understand and resolve issue quickly.

### Scenario B: Preemptive Validation
- **Context:** System disables unavailable options or warns before confirmation.
- **Action:** Parent is prevented from entering excessive amounts.
- **Actor:** Parent
- **Goal:** Avoid failed transactions.

#### User Goal
- To resolve issues with minimal frustration and guidance.

#### Business Goal
- Reduce failed transactions and support positive user experience.

#### Screens

##### Er.5 Insufficient Funds Error (Pre-Transfer)
- **Page Goal:** Prevent invalid input.
- **Screen Description:**
  - Inline error, grayed-out confirmation, suggestion to lower amount or select another account.
- **Design Problems:**
  - HMW avoid unnecessary steps?

##### Er.6 Insufficient Funds Error (Post-Transfer)
- **Page Goal:** Explain failed transfer and next steps.
- **Screen Description:**
  - Error message, retry, help options.
- **Design Problems:**
  - HMW support resolution?

#### Sequence: Er.5 (pre-transfer) OR 2.0 -> 2.1 -> Er.6 (post-transfer)

---

## Summary of Screen Sequences per Scenario

**1. Access Dashboard:**
- 1.0 Youth Account Dashboard -> 1.1 Dashboard - Notification Highlight State / Er.1 Dashboard Load Error

**2. Allocate Funds:**
- 2.0 Fund Transfer Initiation -> 2.1 Transfer Confirmation -> 2.2 Transfer Success / Er.2 Insufficient Balance Error
- Alternate: Pu.1 Quick Transfer Pop-up -> 2.2 / Er.2

**3. Set Spending Limit:**
- 3.0 Spending Limit Configuration -> 3.1 Limit Confirmation -> 3.2 Limit Set Success / Er.3 Invalid Limit Entry
- Alternate: Pu.2 Guided Limit Recommendation -> 3.1 -> 3.2

**4. View Activity:**
- 4.0 Activity List -> 4.1 Filtered Results / Er.4 No Transactions State

**5. Insufficient Balance:**
- Er.5 Insufficient Funds Error (Pre-Transfer) OR 2.0 -> 2.1 -> Er.6 (Post-Transfer)

---

## Accessibility & Scalability Considerations
- All screens support keyboard navigation and screen readers.
- Color contrast and font size meet WCAG 2.1 AA standards.
- Responsive layouts for desktop, tablet, and mobile.
- Error messages are clear, actionable, and non-technical.
- Workflows allow for future features (e.g., recurring transfers, multiple youth accounts).

---

## Minimum Viable Experience (MVE)
- Parent logs in, accesses dashboard (1.0), views balance and recent activity.
- Initiates fund transfer (2.0), confirms (2.1), sees success (2.2) or error (Er.2).
- Sets spending limit (3.0), confirms (3.1), sees success (3.2).
- Views youth activity (4.0), filters as needed (4.1).
- Handles errors gracefully (Er.1, Er.2, Er.3, Er.4, Er.5, Er.6).

---

# END OF UX WORKFLOW DOCUMENTATION
