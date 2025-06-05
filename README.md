<h2 align="center">E-Commerce Purchase Intent Prediction</h2>
<h4 align="center">Machine Learning Pipeline: Preprocessing → Modeling → Evaluation</h4>

<h3>📁 Dataset</h3>
<ul>
  <li><strong>2,250 user sessions</strong> (1,800 train / 450 test)</li>
  <li><strong>Features:</strong> Time on site, pages viewed, cart value, ad clicks, referral source, last ad seen, browser refresh rate (noise)</li>
</ul>

<h3>⚙️ Preprocessing</h3>
<ul>
  <li>One-hot encoding (drop-first) for categorical features </li>
  <li>Outlier capping + optional Yeo–Johnson transforms</li>
  <li>Min–max scaling (applied selectively)</li>
</ul>

<h3>🤖 Models Compared</h3>
<ul>
  <li>Logistic Regression (with/without power transforms)</li>
  <li>Support Vector Machine</li>
  <li>K-Nearest Neighbors</li>
  <li>Decision Tree/Random Forest</li>
  <li>AdaBoost (decision stumps)</li>
  <li>Gradient Boosting</li>
  <li>Voting Ensemble</li>
</ul>

<h3>🔑 Key Findings</h3>
<table>
  <tr>
    <th>Category</th>
    <th>Insight</th>
  </tr>
  <tr>
    <td><strong>Scaling</strong></td>
    <td>Critical for SVM/KNN (<a href="https://scikit-learn.org/">scikit-learn</a>), unnecessary for tree-based models</td>
  </tr>
  <tr>
    <td><strong>Transforms</strong></td>
    <td>Yeo–Johnson didn't improve logistic regression (<a href="https://stats.stackexchange.com/">stats.SE</a>)</td>
  </tr>
  <tr>
    <td><strong>Ensembles</strong></td>
    <td>Voting/Boosting achieved 80% accuracy vs 75–78% for individual models</td>
  </tr>
</table>

<h3>💡 Best Practices Implemented</h3>
<ul>
  <li>Feature scaling tailored to algorithm requirements</li>
  <li>Multicollinearity prevention in categorical encoding</li>
  <li>Comparative analysis of model families</li>
  <li>Ensemble strategies for robust performance</li>
</ul>

<h3>📚 References</h3>
<ul>
  <li><a href="https://www.learndatasci.com/">LearnDataSci</a> - Encoding practices</li>
  <li><a href="https://scikit-learn.org/">scikit-learn</a> - Code was implemented using scikit learn</li>
</ul>

