The Impact of Socio-Economic and Family Factors on Children's Mental Health in the U.S.
An in-depth analysis combining individual-level survey data with state-level socio-economic indicators.

📍 Project Overview
This project conducts a comprehensive analysis of children's well-being in the United States, exploring the intricate relationships between childhood stress, family support systems, and the broader socio-economic environment.

The core uniqueness of this analysis lies in its multi-level approach. By merging two powerful datasets, we investigate children's mental health through both a micro-level lens (individual experiences and family dynamics) and a macro-level lens (state-wide economic and social indicators), providing a holistic view of the factors at play.

❓ Key Research Questions
This project sought to answer the following questions:

How are Adverse Childhood Experiences (ACEs) associated with children's mental health?

Can positive family factors, such as good communication, act as a "buffer" against the stress of ACEs?

How does a state's economic condition (e.g., poverty rate) correlate with the prevalence of behavioral problems in children?

Is a state's education level associated with parents' feelings of neighborhood safety?

Does a relationship exist between housing stability (renter vs. owner-occupied) and child depression at the state level?

📊 Data Sources & Tools
Data Sources:

National Survey of Children’s Health (NSCH) 2023: Provided individual-level data on children's health, family life, and adverse experiences.

American Community Survey (ACS) 2023 5-Year Estimates: Provided state-level socio-economic data, accessed via the Census Bureau API.

Technology Stack:

Analysis: Python, Pandas, NumPy

Statistical Testing: SciPy (Spearman's & Pearson's correlations)

Data Visualization: Matplotlib, Seaborn

Interactive Dashboard: Tableau Public

Environment: Google Colaboratory

🚀 Key Findings & Visualizations
This analysis yielded several key insights, some of which confirmed initial hypotheses while others revealed more complex, non-linear relationships.

Finding 1: ACEs are a Powerful Risk Factor for Behavioral Problems
The analysis revealed a strong, dose-response relationship between the number of ACEs a child experiences and the likelihood of having behavioral problems. The association with behavioral problems was found to be substantially stronger than the link with depression.

[IMAGE: Insert the "Prevalence of Behavioral Problems by ACE Score" bar chart here]

Statistical Evidence: A Spearman's correlation test confirmed a significant, positive relationship (rho = 0.1037, p < 0.001).

Finding 2: The "Buffering Hypothesis" is More Complex Than Assumed
Our initial hypothesis was that good family communication would simply weaken the link between ACEs and depression. The data revealed a more nuanced reality: the very nature of the relationship is different. For children with good communication, the link is weak and linear. For those with poor communication, the link is complex and non-linear, indicating that a simple "buffering" model is insufficient.

[IMAGE: Insert the diagnostic "Point Plot for communication" here]

Statistical Evidence: In the poor communication group, the correlation was unexpectedly negative (rho = -0.1227), highlighting a complex, non-monotonic relationship that warrants further study.

Finding 3: State-Level Economy is Significantly Linked to Child Welfare
At the macro level, a state's economic health correlates with children's well-being. We found a moderate, positive linear relationship between a state's poverty rate and its prevalence of child behavioral problems.

[IMAGE: Insert the "Scatter Plot for poverty vs. behavioral problems" here]

Statistical Evidence: A Pearson's correlation test confirmed a statistically significant linear relationship (r = 0.3496, p < 0.05).

Finding 4: Statistical Rigor Over-rules Visual Intuition
Two of our macro-level hypotheses, while appearing plausible on scatter plots, were refuted by statistical testing. We found no statistically significant evidence to support a link between:

A state's education level and parents' perception of safety (p > 0.05).

A state's percentage of renters and the prevalence of child depression (p > 0.05).

This was a critical finding, underscoring the importance of statistical validation to avoid drawing conclusions from potentially random patterns in the data.

🖥️ Interactive Dashboard
To explore the data and findings in more detail, please visit the interactive dashboard created in Tableau Public.

[IMAGE: Insert an attractive screenshot of your Tableau dashboard here]

➡️ View the Interactive Dashboard on Tableau Public
⚙️ How to Reproduce
Clone the repository:

git clone https://github.com/your-username/your-repo-name.git

Download the NSCH data: Obtain the nsch_2023e_topical.sas7bdat file from the official NSCH website and place it in the project directory.

Set up API Key: Get a free API key from the Census Bureau. In the Google Colab notebook, save it as a secret named CENSUS_API_KEY.

Run the notebook: Open Project_Analysis.ipynb in Google Colab and execute the cells sequentially.

🤔 Limitations & Future Work
Limitations:

Correlation vs. Causation: This analysis identifies associations, not causal links.

Self-Reported Data: The NSCH data relies on parental reports, which can be subject to bias.

Ecological Fallacy: State-level correlations do not necessarily apply to individuals within those states.

Future Work:

Advanced Modeling: Employ regression models to control for multiple variables simultaneously and quantify the impact of each factor more precisely.

Geographic Granularity: If data becomes available, repeat the macro-level analysis at the county level to uncover more localized trends.