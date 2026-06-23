# Platform Pricing Strategies & Psychological Pricing Models 💰

## 1. Core Pricing Strategies for Technical Products
Pricing defines how your product captures a slice of the value it creates for users. For platforms, SaaS, and enterprise software, there are four primary monetization frameworks:

* **1. Value-Based Pricing:** Pricing based on the customer's perceived value and ROI rather than the cost of development. 
    * *Example:* Charging an enterprise \$50k/year for an automation tool because it saves them \$200k/year in manual labor costs.
* **2. Usage-Based / Metered Pricing:** Charging customers dynamically based on their consumption metrics.
    * *Example:* Cloud infrastructure models charging per gigabyte of data transferred, per API call, or per compute hour.
* **3. Tiered (Good-Better-Best) Pricing:** Offering multiple feature packages at distinct price points to capture different segments of the market simultaneously.
    * *Example:* Starter (Basic Features) -> Professional (Advanced Analytics) -> Enterprise (Custom SLAs & SSO).
* **4. Cost-Plus Pricing:** Calculating the internal cost of infrastructure and engineering, then adding a fixed percentage markup. 
    * *Typical use case:* Custom enterprise integration agreements or hosting partnerships.

---

## 2. Psychological Pricing Models in Software & SaaS
Even in highly rational B2B and technical markets, psychological framing heavily influences procurement and executive sign-off:

| Model | Psychological Mechanism | B2B Enterprise Application |
| :--- | :--- | :--- |
| **Price Anchoring** | Establishing a high premium reference point first so that regular options look highly cost-effective by comparison. | Displaying a high-end "Custom Enterprise" tier right next to a "Professional" tier to make the mid-level tier look highly accessible. |
| **The Decoy Effect** | Introducing a third option that is deliberately priced poorly to nudge customers toward the more expensive flagship option. | Offering a "Software Only" tier for \$80, a "Support Only" tier for \$120, and a "Software + Premium Support" bundle for \$125. |
| **Charm Pricing** | Reducing the left digit by one cent or one dollar (e.g., pricing at \$99 instead of \$100) to trigger a lower subconscious price perception. | Used heavily in self-service developer tiers (e.g., API access for \$49/month instead of \$50/month). |
| **Per-User/Per-Seat Unbundling** | Breaking a massive flat-rate platform fee down into digestible, per-user pricing frames. | Reframing a \$12,000 annual contract as a highly digestible "\$15 per user, per month" commitment. |

---

## 3. TPM Architectural Alignment Checklist
Before finalizing a product's pricing model, a Technical Product Manager must ensure the underlying architecture can support it:

* **If Usage-Based:** Does our platform feature robust, low-latency metering services that accurately capture usage counts without dropping packets or data?
* **If Tiered:** Are our feature flags, entitlement engines, and Role-Based Access Controls (RBAC) modular enough to dynamically switch off premium capabilities based on a user's subscription tier?
* **If Enterprise-Tiered:** Are specialized features like Single Sign-On (SSO), data residency locality, and dedicated database clusters decoupled cleanly from the core application stack?
