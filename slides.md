---
marp: true
theme: product-docs
paginate: true
footer: "Page $[page]/$[total]"
---

<!-- _class: lead -->

# Product X – Developer Documentation

### Marp-based Presentation

**Author:** Technical Writer  
**Contact:** 23f3001275@ds.study.iitm.ac.in  

📌 *Version-controlled documentation using Marp.*

---

## Why Marp for Product Documentation?

- 🔐 Single **source of truth** in Markdown  
- 📦 Works with **Git & pull requests**  
- 🔁 Export to:
  - PDF
  - HTML
  - PPTX (via Marp CLI)

---

## Project Structure (Docs-as-Code)

```text
docs/
  ├─ slides.md        # Marp presentation (this file)
  ├─ product-docs-theme.css
  ├─ api-reference/
  └─ guides/
🛠 Keep docs next to the code, update via PR. ``

<!-- _class: lead --> <!-- BACKGROUND IMAGE SLIDE -->

# High-Level Data Flow
Client → API Gateway → Core Service → Worker Queue → Database

## Algorithmic Complexity (Example)
Batch processing:

### Naive approach:
$$ 𝑇
(
𝑛
)
=
𝑂
(
𝑛
2
)
T(n)=O(n 
2
 ) $$

### Optimized (Hash Map):
$$ 𝑇
(
𝑛
)
=
𝑂
(
𝑛
)
T(n)=O(n) $$

Used for request de-duplication and idempotency.

# Sample Client Code (JavaScript)
js
Copy code
async function createOrder(order) {
  const res = await fetch("https://api.example.com/v1/orders", {
    method: "POST",
    headers: { "Content-Type": "application/json" },
    body: JSON.stringify(order)
  });
  if (!res.ok) throw new Error("API Error");
  return res.json();
}
Versioning & Release Notes
Semantic versioning

v1.x — stable

v2.x — beta + breaking

Every release:

Update CHANGELOG

Regenerate PDF/PPTX through Marp

<!-- _class: lead -->
Contact
📧 23f3001275@ds.study.iitm.ac.in
💬 Feedback? PRs welcome!
