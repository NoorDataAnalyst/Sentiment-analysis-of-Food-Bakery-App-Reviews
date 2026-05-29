#  Food & Bakery App Reviews: Sentiment Analysis & Topic Modeling

A Text Mining and Topic Modeling project applying Latent Dirichlet Allocation (LDA) to customer reviews across 10 major cookie, bakery, and food delivery applications. This project goes beyond basic star ratings to extract actionable business insights from unstructured user feedback.

---

##  Authors (Group Members)
* **Azka Aziz** (FA24-BBD-023)
* **Noor Ul Ain Zahid** (FA24-BBD-069)
* **Rida Chaudary** (FA24-BBD-075)

**Course:** Bachelor of Business Data Analytics  
**Institution:** COMSATS University Islamabad, Lahore Campus  
**Submitted To:** Prof. Abdul Hannan

---

##  Project Overview
Mobile apps have become the primary storefront for modern bakeries and food retailers. This project applies unsupervised machine learning to discover latent thematic structures within customer text reviews. By building a text mining pipeline in R, we analyzed consumer expectations, app usability flaws, and logistical bottlenecks across 10 prominent apps.

### Target Applications Covered
* **Cookie Specialists:** Crumbl Cookies (`com.blink.crumblecookies`), Insomnia Cookies (`com.insomniacookies.insomnia`)
* **Local Bakeries:** Layers Bakeshop (`pk.layers.twa`), Hobnob Bakery (`com.indolj.hobnob`), Jamil Sweets (`com.blink.jamilsweets`), Jalal Sons (`com.tossdown.jalalsons`), Kitchen Cuisine (`com.cuisine.kitchen`), Tossdown Shezan (`com.tossdown.shezan`)
* **Food Delivery & Marts:** Gourmet GMart (`com.gourmet_foods.GMart`), The Pits (`com.blink.pits`)

---

##  Technical Workflow & Methodology

### 1. Text Preprocessing Pipeline
To prepare raw reviews for modeling, data is structured and cleaned using the `tm` package in R:
* Text normalization by mapping strings to lowercase
* Elimination of punctuation, numbers, and standard English stopwords
* Stripping out generic application noise words (such as "app", "order", "cooki", and specific brand names) to find deeper structural insights
* Stemming words to their linguistic roots to compile a clean Document-Term Matrix (DTM)

### 2. Finding the Optimal Topic Count ($K$)
We evaluated the optimal number of latent topics by plotting **Perplexity Scores** across a sequential testing range from $K = 2$ to $K = 20$. The empirical model performance showed a visible drop in perplexity from ~286 down to ~238 as the structural groupings expanded, confirming a rich, multi-layered mix of customer feedback.
<img width="840" height="840" alt="1" src="https://github.com/user-attachments/assets/d9ace6b0-d632-4e50-ade5-2543b3a4bcad" />
<img width="840" height="840" alt="2" src="https://github.com/user-attachments/assets/80f47a20-345b-4023-b2c6-3cae8d8169e3" />


---

##  Core Findings & Interpretations
The text mining engine categorized customer sentiment into three main operational pillars:

### Pillar 1: App Performance and Usability (Software Engineering)
* **Top Keywords:** `work` (339 times), `use` (342 times), `updat` (156 times)
* **Insight:** Users frequently express frustration regarding technical bugs, broken updates, lagging interfaces, and checkout screen freezes.

### Pillar 2: Delivery & Ordering Logistics (Operations)
* **Top Keywords:** `order` (875 times), `deliveri` (316 times), `servic` (301 times), `easi` (297 times), `time` (270 times)
* **Insight:** For temperature-sensitive items like warm cookies or fresh cakes, delivery speed and reliable tracking are critical to customer satisfaction.

### Pillar 3: Product Quality & Food Satisfaction (Core Offering)
* **Top Keywords:** `good` (556 times), `best` (406 times), `love` (361 times), `great` (308 times)
* **Insight:** Consumer sentiment regarding food quality is overwhelmingly positive. Brand loyalty is anchored firmly in product taste and freshness.
<img width="1348" height="876" alt="WhatsApp Image 2026-05-22 at 3 48 34 PM" src="https://github.com/user-attachments/assets/f8078284-53e8-4b2b-96b3-030195e77e3c" />

---

##  Strategic Recommendations

###  Fix the Technical Foundation First
A broken digital storefront ruins great food. Engineering teams must prioritize post-update testing, resolve shopping cart lags, and eliminate software crashes on payment screens.

###  Upgrade Order Tracking Transparency
Since delivery timing is a major consumer focus area, brands should introduce real-time delivery tracking, send automated SMS alerts, and establish strict delivery time windows.

###  Capitalize on Product Loyalty
Marketing campaigns should turn high-frequency praise words like "best" and "love" into social proof. Highlight user-generated reviews and pair them with loyalty rewards to increase app-based sales.

---

##  Repository Structure
```text
├── README.md               # Project documentation and summary
├── ML_Project_file.ipynb   # R notebook containing text preprocessing and LDA modeling
└── Data/                   # Directory for raw and processed application review text files
