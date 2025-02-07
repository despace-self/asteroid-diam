# asteroid-diam
This contains the findings from a JPL open asteroid dataset exploration attempt by me.

I recently worked on a machine learning experiment using asteroid data officially maintained by the Jet Propulsion Laboratory (JPL) of the California Institute of Technology, which operates under NASA. This dataset includes extensive information on asteroids, including orbital parameters, physical properties, and observational details. It is publicly available at JPL's Small-Body Database Query.

Approach
The dataset originally contained 958,524 asteroid entries with various attributes. My goal was to predict the asteroid diameter, a key property in understanding an asteroid’s physical characteristics.

Key challenges:

The dataset had only 136,209 available diameter values, while 823,421 albedo values were missing.
Theoretical diameter can be estimated using H (absolute magnitude) and albedo using a well-known formula.
I first extracted the available values and trained a neural network to predict asteroid diameters.
Results
The first model achieved Test Mean Squared Error (MSE): 5.2933 and R² Score: 0.9539, indicating strong predictive performance.
To fill in the missing diameter values, I trained a proxy model using a different approach, which resulted in MSE: 2.2111 on available target values.
However, when I used the first model to test the proxy-predicted dataset, it performed worse, with a significantly larger MSE.
Takeaways
This suggests possible overfitting to the known diameters or inconsistencies in how missing values were imputed. Further improvements could include:

Exploring alternative regression models or ensemble learning.
Incorporating additional asteroid parameters to improve feature representation.
Testing different neural network architectures and hyperparameter tuning.
Investigating potential biases in the dataset.
This experiment provided valuable insights into asteroid data prediction, and I hope to refine this approach further. Would love to hear thoughts and feedback!

Code available on:
Kaggle Notebook

#MachineLearning #DataScience #Asteroids #NASA #DeepLearning
