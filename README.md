#ML Visualization Dashboard
An interactive, browser-based tool for building intuition around six core machine learning algorithms — no training required to explore, just sliders, clicks, and step buttons.
Most ML explanations show you a static diagram or a wall of math. This dashboard lets you nudge the parameters yourself and watch the model react in real time: a decision boundary bending, a loss curve dropping, a cluster reshuffling.
#Algorithms covered
     Linear Regression — adjust slope/intercept manually or run gradient      descent step-by-step and watch the loss curve converge
     Logistic Regression — train the model, then slide the decision           threshold and watch the boundary shift independently of the data
    K-Nearest Neighbors — click anywhere to drop a test point, see it
    k nearest neighbors highlighted, toggle shaded decision regions
    Decision Tree — adjust max depth and watch the recursive, Gini-          impurity-based axis-aligned splits carve up the feature space
    K-Means Clustering — step through assignment/update iterations, run      to convergence, or reinitialize to see how starting position             changes the result
    Naive Bayes — a Gaussian per-class model with a probability-             confidence heatmap; shift the class prior and see the boundary bend      without touching the underlying data
Each panel includes a short "field notes" explanation of what's on screen, so it doubles as a reference, not just a toy.
Tech
Single-file HTML/CSS/vanilla JS — no framework, no build step, no dependencies. All algorithms (gradient descent, KNN, recursive tree splitting, k-means, Gaussian NB) are implemented from scratch in plain JavaScript, rendered on HTML canvas. Runs entirely client-side, which also makes it light enough to run comfortably on low-spec hardware.
Run it
Just open ml-visualization-dashboard.html in any modern browser. No installation, no server.
#Why I built this
I'm a second-year AI/ML engineering student, and I kept noticing that the algorithms that felt hardest to internalize weren't hard because of the math — they were hard because I'd never seen them behave. This is my attempt to fix that for myself, and to make it available for other learners hitting the same wall. It was built with the help of AI coding tools directing the implementation, from a fairly detailed spec of what each panel needed to teach.
#What's next
Let users upload their own small CSV datasets to see the same algorithms behave on real data
Add a comparison mode (e.g. same dataset across KNN vs Decision Tree vs Naive Bayes)
Companion Matplotlib cheat sheet (confusion matrices, ROC curves, loss curves, decision boundaries) — already built separately, could be merged in as a reference tab
