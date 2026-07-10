# Premium Bordereaux Analysis

Exploratory analysis of an insurance premium bordereaux dataset, examining
premium volume, claims behavior, and loss ratios across branches, product
lines, and distribution channels.

## Data

The dataset used in this project is fully synthetic, generated to mirror
the structure and realistic value ranges of a real insurance premium
bordereaux report. No real customer or company data is included.

## Questions Explored

- How is policy volume and premium distributed across branches and product lines?
- What is the claims frequency and average loss ratio by product line?
- Is there a relationship between how often a product is claimed on and how severe those claims are?
- What is the split between new and renewal business, and does loss ratio differ between them?
- Which branches carry the highest loss ratios?

## Key Findings

- **Premium is concentrated but not dominated by one branch** — Branch 103
  leads in total premium (~KES 210M), roughly 35% higher than the lowest
  branch (101, ~KES 155M).
- **Engineering and fire products carry the highest loss ratios** —
  ENG-Contractor All Risk, ENG-Erection All Risk, and Fire Domestic Package
  top the list, consistent with their exposure to large, infrequent losses
  typical of these classes.
- **Claims frequency and loss ratio move together, not in trade-off** —
  products with higher claims frequency also tend to show higher average
  loss ratios, rather than the classic "frequent-but-small vs rare-but-severe"
  pattern.
- **New business runs a slightly higher loss ratio than renewals**
  (0.0086 vs 0.0074), plausibly because renewed policies are already
  proven, lower-risk business, while new business is unknown risk in its
  first year.
- **The book is close to evenly split** between new (51%) and renewal (49%) business.
- **Branch 105 stands out with a notably higher loss ratio (~0.0102)** 
  compared to the rest of the network, which clusters between 0.006–0.0087, 
  making it a candidate for closer underwriting review. Branch 106 shows 
  the lowest loss ratio (~0.006).

## Visualizations

1. Total gross premium by branch
2. Total gross premium by product line
3. Average loss ratio by product line (color-scaled)
4. Claims frequency vs. loss ratio by product, sized by total premium
5. New vs. renewal business mix
6. Average loss ratio by branch (color-scaled)

## Tools

Python, pandas, Plotly (`graph_objects`)

## How to Run

1. Clone this repo
2. `pip install pandas plotly`
3. Open `notebooks/eda.ipynb` in VS Code or Jupyter
4. Run all cells — data is loaded via a relative path from `data/`

