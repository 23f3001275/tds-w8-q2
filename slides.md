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
🛠 Keep docs next to the code, update via PR.
```

---

<!-- BACKGROUND IMAGE (VALID MARP SLIDE) -->
![bg](https://images.pexels.com/photos/1181671/pexels-photo-1181671.jpeg)

---

# High-Level Data Flow
Client → API Gateway → Core Service → Worker Queue → Database

## Algorithmic Complexity (Example)
Batch processing:

### Naive approach:
$$T(n) = O(n^2)$$

### Optimized (Hash Map):
$$T(n) = O(n)$$

Used for request de-duplication and idempotency.

# Sample Client Code (JavaScript)
```
async function createOrder(order) {
  const res = await fetch("https://api.example.com/v1/orders", {
    method: "POST",
    headers: { "Content-Type": "application/json" },
    body: JSON.stringify(order)
  });
  if (!res.ok) throw new Error("API Error");
  return res.json();
}
```

### Versioning & Release Notes
#### Semantic versioning

* `v1.x` — stable
* `v2.x` — beta + breaking

#### Every release:
* Update CHANGELOG
* Regenerate PDF/PPTX through Marp

<!-- _class: lead -->
### Contact
* 📧 [23f3001275@ds.study.iitm.ac.in](23f3001275@ds.study.iitm.ac.in)
* 💬 Feedback? PRs welcome!
