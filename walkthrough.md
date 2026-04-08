# Ditto · MPG Demo Walkthrough Script

**Suggested run time: 12–15 minutes**

---

## 0 · Opening (30 seconds)

> "Thanks for making time. What I'm going to show you is a private, secure AI workspace we'd deploy specifically for MPG — sitting alongside Xero and Xero Practice Manager, not replacing anything. I'll start by showing you how it's built and where your data lives, then walk through the three things it actually does day-to-day."

**Click:** `🏗 Architecture` tab.

---

## 1 · Architecture (2–3 minutes)

> "Before I show you any of the AI magic, I want to answer the question every partner asks first: *where does my client data go?* Because the answer has to be bulletproof."

Start at the **top** and walk down.

**Top — MPG Staff**
> "Everything starts with you — your partners and team logging in from their own browser."

**Perimeter — Web Application Firewall + Transport Layer Security**
> "Every request hits the AWS perimeter first. The Web Application Firewall blocks common attacks before they ever reach the application, and Transport Layer Security encrypts the traffic in transit. Standard, but important."

**Dashed container — Ditto Secure Infrastructure**
> "Everything inside this dashed boundary is our private AWS environment in Sydney. Private network, encrypted at rest, monitored, fully logged."

**Click the Staff Interface box** (shows side panel).
> "This is the web app you and your team actually use — single sign-on, multi-factor login, role-based access, and a full audit trail. Every click is recorded."

**Click the Ditto Middleware box** (lime — highlights).
> "This is the core of our platform. It authenticates every request, pulls data from Xero and XPM only when it's needed, uses it, and immediately throws it away."

Point to the **Xero / Xero Practice Manager** boxes on the right.
> "Notice these sit *outside* the secure boundary — because they're *your* systems. Ditto reaches out via delegated authorisation, pulls exactly what it needs, processes it, and discards the raw data. Nothing is copied or stored."

**Click the Credential Vault / Least-Privilege Access / Private Network Routes badges.**
> "Your Xero and XPM tokens live in an encrypted vault, the application role has the narrowest possible permissions, and traffic between our services never touches the public internet."

**Click the Private Language Model box** (purple).
> "This is where the AI runs — Claude, delivered through AWS Bedrock, in the Sydney region. Crucially: no prompts are logged, no client data is ever used to train a model, and your data never touches a public AI endpoint like ChatGPT."

Point to the monitoring strip at the bottom.
> "And the whole platform is continuously observed — real-time metrics, threat detection, and a 7-year audit trail available for client audit on request."

**Hover the three orange output boxes.**
> "And this is what the platform actually does for you — three AI modules that run directly against your Xero and XPM data. Let me show you each one."

> *Optional line:* "By the way, everything on this diagram is exportable — I can hand you the SVG or a high-res PNG for your board paper."

---

## 2 · Dashboard (2 minutes)

**Click:** `🏠 Dashboard` tab.

> "This is the first screen you'd see every morning. Ditto has already done the overnight work — it's connected to Xero and XPM, pulled status across 142 clients, and it's telling me what actually needs my attention today."

Point to the **welcome strip** (dark hero bar).
> "'Good morning Michael — Ditto has already handled 14 tasks for you overnight.' Every morning, before you've even had your coffee."

Point to the **4 KPI tiles**.
> "Top-line health of the practice — revenue month-to-date, unbilled work in progress, cash in the bank, active jobs. All live from Xero."

Point to the **⚡ Needs Your Attention** card.
> "This is the important one. Ditto has ranked five things for me, most urgent at the top."

> "It's spotted that two tax returns are now overdue — Harbour Cafe and Aoraki Consulting — and it's already drafted reminder emails for me to review. I just click through."

**Click that critical item.** It jumps to the Tax Reminders tab. Don't run anything yet — click back to Dashboard.

> "It's also flagged two unusual transactions on our practice account for review — a possible duplicate payment and an unsupported cash withdrawal."

Point to the **Ditto AI hero tile** (black card with lime "4h 32m").
> "And this is the number that gets partners excited — **4 hours 32 minutes saved** by automation in the last week. 47 client reminders sent, 212 transactions coded, 18 reports drafted — while we were asleep."

Point to the **Activity Feed** below it.
> "Live feed of everything Ditto has done — every action timestamped, every client tracked."

Point to the **Client Health Watchlist**.
> "Ditto continuously scores your entire client book on revenue trend, margin, cash runway, and debtor days. Harbour Cafe is in the red — 32 out of 100 — and it's telling me why."

Point to **Team Workload**.
> "And it's watching capacity. Michael's at 92% — Ditto would nudge me to reassign new jobs to Sarah or James before I burn myself out."

> "Now let me show you the three AI workflows this all plugs into."

**Click:** `📊 Financial Narratives` tab.

---

## 3 · Financial Narratives (3 minutes)

> "First module: AI financial commentary. This is the one that saves the most hours on a typical month-end."

Point to the **client picker**.
> "I can pick any of my reporting clients from the dropdown — same list that's in XPM."

**Select Kiwi Build Supplies Ltd.**
> "Pulled straight from Xero — full March P&L, YoY deltas, account-level breakdown, GST position, everything. This is read-only — Ditto isn't changing your Xero file, just reading it."

Point to the **KPI cards** with sparklines.
> "Revenue up 12.4%, expenses up 18.7%, net profit up 4.1%, GST payable of $8,420 due on the 28th. All live."

**Click `⚡ Generate AI Narrative`.**

> "Now watch. Ditto is reading the P&L, comparing it against the prior three months and year-on-year, detecting variances above a 10% threshold, analysing cashflow and aged receivables, and drafting a client-ready commentary in MPG's house style."

The five-step AI panel animates through, then the report types itself out.

> "That's a full five-paragraph report — executive summary, revenue analysis, cost variances, cashflow observation, and specific recommended actions — written in plain English, ready to send to the client. It took about **fifteen seconds**. Normally that's a partner with a calculator for twenty minutes."

Point to the **Edit Report** button.
> "If I don't like a paragraph, I click Edit, rewrite it in place, hit save. Ditto learns MPG's tone over time."

Point to the **action buttons**.
> "Then I can download it as a branded PDF, send it straight to the client from Ditto, or attach it back to the XPM job — all one click."

**Quickly switch clients** (e.g. to Harbour Cafe).
> "Different client, different story. Harbour Cafe's revenue is sliding. Watch — Ditto generates an entirely different narrative with completely different recommendations."

**Click:** `📬 Tax Reminders` tab.

---

## 4 · Tax Reminders (2–3 minutes)

> "Second module — the one that gets your clients to send you their records on time."

Point to the **filter chips** at the top.
> "Full XPM job list — 8 active tax jobs, 2 overdue, 3 due this week, 3 already lodged. Pulled straight from XPM, including IRD numbers, return types, periods, due dates and who they're assigned to."

**Filter to `Overdue`.**
> "These two are the problem. Harbour Cafe's GST return was due 31 March — I've probably been meaning to chase them for a week."

**Switch back to `All`.**

Point to the **Review before send / Auto-send toggle**.
> "Here's something important — I can run this on autopilot, but most partners want to approve every email before it goes out. That's the default."

**Click `⚡ Run AI Automation`.**

> "Ditto is now working through each client that needs a nudge. It knows who's overdue, who's due soon, who's already lodged. For each one that needs a chase, it's drafting a personalised email."

Emails appear one at a time and type themselves out.

> "Look at the first one — 'Hi Sarah, a quick note from the team at MPG — your February GST return is now overdue…' — it even knows the return type and the due date. And it's politely chasing her for the Hubdoc uploads. Every email is different — the next one references the specific things Ditto knows are missing for that client."

Point to the **approve/edit/discard buttons** on each email.
> "I can edit the wording, approve it, or discard it. Once I approve, the row updates to 'Sent · Logged to XPM' — the outcome is written back to the XPM job automatically."

**Approve one or two.**
> "Imagine doing this for 40 clients at the end of every month. That's where the real hours come back."

**Click:** `⚡ Bank Reconciliation` tab.

---

## 5 · Bank Reconciliation (2–3 minutes)

> "Last module — and this is the one that makes your bookkeeper very happy. AI bank reconciliation for your *own* practice account."

Point to the **rec header** — ANZ practice account, balances, unreconciled count.
> "This is MPG's own ANZ practice account — 12 unreconciled statement lines for March, just like you'd see in Xero."

Walk down the **transaction list**.
> "Software subscriptions, fuel, office supplies, CPA membership, a payment to 'JBT Holdings' that we don't recognise, a $500 ATM withdrawal. Mix of the routine and the problematic — typical end-of-month."

**Click `⚡ Run AI Coding`.**

> "Ditto is now parsing every line, matching against your Xero chart of accounts — 274 accounts — applying MPG's own coding rules and GST treatment, and flagging anything that looks suspicious."

Watch the five-step AI panel run, then the rows animate one by one.

> "Look — 99% confidence on the Xero subscription, 96% on the Z Energy fuel, 97% on Officemax, 94% on the CPA membership. Full account code, GST treatment applied, ready to post."

When it reaches the **JBT Holdings and ATM withdrawal** rows.
> "And here are the two it's not confident about. 'JBT Holdings' — no prior history, and the amount matches a payment to the same account on 28 February. Ditto thinks it might be a duplicate. And the ATM withdrawal — no receipt in Hubdoc, so it can't code it without partner review."

Scroll down to the **summary tiles**.
> "10 transactions coded automatically, 2 flagged for review, average confidence 95%, and **38 minutes saved** versus manual coding. On just one account for one month."

Scroll to the **Review Queue** that appears.
> "Here are the two flagged items, with smart next-step options for each one. For the possible duplicate — 'Compare to 28 Feb', 'Query with the bank', or 'Assign to partner'. For the ATM withdrawal — 'Request receipt', 'Assign to partner', or 'Code as drawings'."

**Click a resolution option.**
> "Resolved. Ditto logs what I did, applies the coding, and once everything is cleared the 'Post to Xero' button unlocks and pushes the whole batch back to Xero in one click."

**Click `✓ Post to Xero`.**
> "Done. Reconciled, posted, audit trail captured."

---

## 6 · AI Assistant (2–3 minutes)

**Click:** `🤖 AI Assistant` tab.

> "The last thing I want to show you — and this is where it starts to feel less like software and more like having someone on your team. This is the AI Assistant. Instead of going into each module separately, your team can just ask."

**Click the suggestion chip: "Which clients are overdue?"**

Wait for the tool call indicator and response to complete.

> "See that line — checking XPM, get clients, status overdue — that's the AI deciding what data it needs and going to get it. Zabeen didn't tell it where to look. It just knew."

*[pause]*

> "Three clients, overdue, right there. And now it's offering to draft the reminders in one go."

**Click "Draft all three reminders".**

Wait for the draft to appear.

> "That's a notice ready for Michael's approval. Nobody wrote that — the AI pulled the client details from XPM and drafted it in MPG's voice. And nothing gets sent until a human confirms it."

*[pause]*

> "Let me show you one more."

**Type "Show me the March P&L" in the input field and press Enter.**

Wait for response.

> "Revenue, expenses, margin — pulled live from Xero. And it's already flagged something. A software transaction it doesn't recognise. It's not just reporting the data, it's reading it."

*[pause — let Michael absorb]*

> "This is what we mean by done for you. Your team doesn't learn a new system. They just ask, review, and approve. The AI does the rest."

---

## 7 · Close (1 minute)

> "So that's the full picture — reporting, notice automation, accounts processing, an AI assistant, and the secure architecture underpinning all of it."

> "The question for today is where you want to start. What's costing your team the most time right now?"

---

## Presenter tips

- **Presenter dot** (bottom-left) is on by default — your cursor glows lime so viewers can follow you on a shared screen.
- Click the **settings cog** in the top-right to jump to the Setup tab mid-demo if they ask "can it be rebranded?" — show them the logo upload and client rename fields, then jump back.
- If the client derails onto security questions, click any component on the Architecture tab — the side panel answer is already written in plain English.
- Every "Send to Client", "Export PDF", "Attach to XPM Job" and "Post to Xero" button is a mock popup — call it out if someone asks to actually click send.
