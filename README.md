# ReturnOS

**Live demo:** https://returnos.netlify.app

ReturnOS is a browser-based prototype for item-level e-commerce returns and refunds. It helps customers and operations teams understand what happens to each returned item when eligibility rules, pickup evidence, inspection decisions, payment instruments, and external status updates do not line up.

> **Prototype notice:** This is a simulated demo. It does not contact real sellers, couriers, banks, or payment providers. Do not enter real customer or payment information.

## What you can explore

- Review return eligibility and remedy options before submitting a request.
- Follow separate return journeys for each item in a mixed-seller order.
- See a line-by-line refund preview across card, wallet, voucher, and discounts.
- Resolve failed-pickup claims with attempt evidence, rescheduling, and drop-off options.
- Review an inspection decision, compare handover evidence, and appeal the outcome.
- Reconcile platform, seller, and payment-provider statuses as **waiting**, **stuck**, or **needs review**.
- Trigger a refund retry and see idempotency prevent a duplicate payout.
- Explore proportionate fraud friction, fairness checks, and customer message previews.
- Review and export the simulated event audit.

## Run locally

No build tools, package installation, or server are required.

1. Download or clone this repository.
2. Open `index.html` in a modern browser.
3. Use **Reset demo** in the app to restore the seeded scenario.

The prototype saves its demo state in the browser's local storage. Clearing site data or using another browser starts a separate demo state.

## Publish with GitHub and Vercel

1. Add `index.html`, `app.js`, `styles.css`, and `README.md` to the repository root.
2. Push the repository to GitHub.
3. Import that GitHub repository into Vercel.
4. Use the project root as the root directory. No framework, build command, environment variables, or output folder is required for this plain static site.

## Demo scenario

The seeded order contains four items from three sellers, paid with a card, wallet balance, voucher, and order discount. Two items are returned. The walkthrough includes two disputed pickup attempts, an inspection hold, a voucher-versus-card refund split, a provider-versus-seller status mismatch, and a legitimate frequent returner.

All amounts, identities, policies, timestamps, external statuses, and review outcomes are illustrative and simulated. A provider status such as **reversed** does not mean the money has arrived in a bank account.

## Production boundary

This prototype uses client-side state and local storage. It does not provide authentication, server-side policy enforcement, payment or courier integrations, durable audit storage, or production privacy controls. A production system would need secure APIs, provider-specific status semantics, server-side idempotency, access controls, versioned policies, durable event storage, and tested customer communications.
