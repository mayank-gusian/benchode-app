# BENCHODE 💻📊

## Project Overview
Benchmark Engine for Not-yet-tested Computers with Heuristic Optimization &amp; Deals Extractor (BENCHODE). A Next.js PWA that predicts hardware benchmarks via machine learning and aggregates live e-commerce deals across India to deliver smart, persona-based laptop recommendations.

## 🛠️ The Core Engineering Architecture & Tech Stack

To meet our team's requirements for a modern, rapid-prototyping ecosystem that enforces type integrity and catches structural bugs at compile-time, we designed a decoupled, multi-tier system architecture.

| Architectural Layer | Core Technology | Primary Use Case | Engineering Justification ("The Why") |
| :--- | :--- | :--- | :--- |
| **Frontend UI (PWA)** | `Next.js 15 (App Router)` + `TypeScript` | Server-side rendered interface & installable mobile shell. | Provides a robust React foundation with native service-worker compatibility. TypeScript guarantees structural type-safety inside components, mitigating runtime crashes on user devices. |
| **Styling & Components** | `Tailwind CSS` + `shadcn/ui` | Rapid layout prototyping and accessible interface design. | Utility-first styling combined with radix-ui primitives eliminates the need to write monolithic custom CSS files, letting the team focus 100% on core performance logic. |
| **Backend API Engine** | `Next.js Route Handlers` | Core backend routes, persona filtering, and client database access. | Ensures full-stack TypeScript harmony. Consolidating standard API endpoints inside Next.js reduces operational overhead for a 3-person deployment team. |
| **AI / Prediction Engine** | `Python (FastAPI)` + `scikit-learn` | Machine learning forecasting microservice for missing benchmarks. | Scikit-learn offers ultra-lightweight Random Forest Regression for hardware performance estimates. FastAPI isolates this pipeline as a high-performance microservice that auto-documents its endpoints. |
| **Database Layer** | `PostgreSQL` | Relational storage for detailed laptop specifications, pricing arrays, and users. | The highly relational nature of computer hardware (CPUs mapped to multiple GPUs and dynamic store URLs) mandates a robust relational model. |
| **Object-Relational Mapping** | `Prisma ORM` | Safe database querying and programmatic migrations. | Auto-generates runtime TypeScript definitions based on the PostgreSQL database schema. Catches invalid database queries inside VS Code before execution. |
| **Data Scraping Pipeline** | `Playwright` (Node.js/Python) | Automated data harvesting from e-commerce sites (Amazon, Flipkart). | Features excellent programmatic browser automation tools designed to systematically handle asynchronous page loads and dynamically rendered product pricing layout changes. |
| **CI/CD Quality Control** | `GitHub Actions` | Automated code integration, lint enforcement, and type validation checks. | Ensures strict quality controls via a continuous pipeline. Automatically blocks broken branch features from merging into production if TypeScript compilation checks fail. |
| **Production Hosting** | `Vercel` / `Render` | Automated serverless hosting with zero-config Git integrations. | Offers seamless, continuous integration pipelines that instantly rebuild and deploy the live build staging area every single time a Pull Request is safely merged into `main`. |