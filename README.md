## Smart India Hackathon Workshop
# Date: 25.11.2026
## Reference Number: 26015651
## Name: Dineesh Anandan
# <u>Problem Title</u>
SIH 26033: Multiple intermediaries reduce farmers earnings and increase consumer prices.

# <u>Problem Creater's Organization</u>
Ministry of Consumer Affairs, Food & Public Distribution

# <u>Theme</u>
Agriculture, FoodTech & Rural Development

# <u>Problem Description</u>
Expected Solution: Create a digital marketplace that connects farmers/FPOs directly with consumers and bulk buyers, provides logistics support, and uses AI for demand forecasting and route optimization.
* Connects farmers/FPOs directly with consumers and bulk buyers.
* Provides logistics support.
* Uses AI for demand forecasting and route optimization.

## <u>Benefits:</u>
* Better prices for farmers.
* Lower prices for consumers.
* Reduced supply chain inefficiencies.

# <u>Proposed Solution</u>
## <u>Solution Title: Project AgriDirect: Hyperlocal Farm-to-Fork Digital Market & Pooled Cold-Chain Network</u>
AgriDirect is a stack, mobile-first digital supply chain ecosystem that connects individual farmers and Farmer Producer Organizations (FPOs) directly with urban residential communities, retail consumers and B2B bulk buyers (supermarkets, restaurants, hostels). By combining voice-assisted onboarding, AI-assisted quality grading, pooled milk-run logistics and automated UPI escrow settlements, AgriDirect compresses the supply chain from 5+ hops to a single direct route.

## <u>How It Addresses the Problem:</u>
In Indian agricultural supply chains, fresh produce passes through 4 to 6 layers of intermediaries —village aggregators, commission agents (arhatiyas), regional mandi wholesalers, secondary distributors and local retailers—before reaching the end consumer. Each layer adds margins, handling fees and transit delays without adding proportional value (reducing farmer share to 25%–35% of retail price while causing 15%–25% post-harvest wastage). AgriDirect addresses this directly through:
* **Vernacular & Voice-First Farmer Onboarding:** Farmers list harvest quantities in Tamil, Hindi or regional languages using voice-to-text prompts and smartphone photos—eliminating literacy or tech barriers.
* **AI-Driven Quality Grading & Digital Assaying:** An on-device Computer Vision model grades produce size, ripeness and defect percentage from a 5-second video scan, generating a digital quality certificate that builds buyer trust.
* **Algorithmic Fair-Price Discovery:** Our pricing engine benchmarks live e-NAM and AGMARKNET mandi rates against retail demand to recommend a transparent split—increasing farmer realization by 25–40% while lowering consumer prices by 15–25%.
* **Community Group-Buying (Neighborhood Pods):** Urban apartment complexes and residential streets form 'Neighborhood Harvest Pods that aggregate household orders into FPO-sized bulk dispatches, unlocking wholesale transport economics.
* **Pooled Milk-Run & Cold-Chain Logistics:** A Vehicle Routing Problem (VRP) solver dynamically schedules shared mini-trucks and EV cargo vans across Village Collection Centers (VCCs) to pick up aggregated harvests and deliver directly to drop points.
* **Instant Escrow & QR Provenance Traceability:** Buyer payments are held in a UPI-integrated escrow ledger and released directly to the farmers bank account upon QR-verified delivery at the collection/drop hub—ensuring zero payment defaults.

# <u>Technical Approach</u>
The system follows a cloud-native microservices architecture designed for high availability in low bandwidth rural networks (offline-first local caching with background sync) and real-time order matching in urban clusters.
<img width="1600" height="842" alt="SIH_26033_Technical_Architecture_v4" src="https://github.com/user-attachments/assets/fc093a0d-135f-4635-bc2f-942a4ac25603" />


## <u>Technologies to be Used:</u>
* **Frontend & Mobile:** Flutter (Android/iOS), React.js (Web Portal), SQLite Offline Sync, Bhashini Voice API — Offline-capable farmer listing app with regional voice input; consumer & B2B order dashboard.
* **Backend & APIs:** Python (Django / FastAPI), PostgreSQL + PostGIS, Redis Cache, REST & WebSockets — Geospatial matching of farms to nearby demand clusters, order lifecycle management and live tracking.
* **AI & Optimization:** TensorFlow Lite (MobileNetV3), OR-Tools (VRP Solver), Scikit-Learn / XGBoost — On-device produce defect/ripeness grading, dynamic price forecasting and shared fleet route optimization.
* **Trust & Payments:** RazorpayX / UPI AutoPay Escrow, Hyperledger / SHA-256 QR Ledger, e-NAM API — Tamper-proof batch harvest traceability from farm plot to consumer kitchen and instant T+0 farmer payout.

## <u>Methodology and Process for Implementation:</u>
* **Step 1. Digital Harvest Listing:** Farmer records harvest details (crop type, expected yield, harvest window) via voice or simple icons and runs a 5-second camera quality scan.
* **Step 2. Demand Aggregation & Matching:** The platform aggregates village supply through local FPOs/VCCs and displays real-time available stock to urban Neighborhood Pods and B2B buyers.
* **Step 3. Transparent Price Lock & Escrow:** Dynamic pricing locks a farm-gate price plus shared logistics fee, saving consumers ~20% over retail while boosting farmer income by ~30%.
* **Step 4. Pooled Milk-Run Dispatch:** OR-Tools dispatches a pooled vehicle along an optimized village-to-city route; QR codes are scanned at pickup and drop-off.
* **Step 5. Instant Direct Settlement:** Upon QR scan confirmation at the hub, escrow automatically triggers instant UPI disbursement directly into the farmers account.on QR scan confirmation at the hub, escrow automatically 
triggers instant UPI disbursement directly into the farmers account.
