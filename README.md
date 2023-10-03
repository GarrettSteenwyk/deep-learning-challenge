# Deep Learning Challenge Report


*Overview*
This was an exploration into taking data for applicants of a non-profit organization to predict whether or not they would be successful. This was done with machine learning and neural networks, as well as the knowledge of parsing data frames in python to set it up for such systems.

*Preprocessing*
- Target Variable: "IS_SUCCESSFUL"
- Featured Variables: Nearly every other column that was present in the original dataset, however the there were two bins used: one on "APPLICATION_TYPE" and one on "CLASSIFICATION".
![Alt text](Images/application.png?raw=true)
![Alt text](Images/classification.png?raw=true)
- Removed Variables: 'EIN' and 'NAME' columns were dropped due to potential irrelevance.

*Making and using models*
- Initial model used 2 layers with 80 neurons on first and 30 on second (all models used the same number of activation functions (2), did not think of changing that): target was not met
- First optimization increased in layers to 3, with neurons of 30, 70, and 8 respectively, with 10 less epochs (this was for slight time optimizations due to either negligible or nonexistent diminishing returns): slight performance increase but not to target
- Second optimization dropped two more columns, being 'STATUS' and 'SPECIAL_CONSIDERATIONS' (later adding to null performance); neuron counts now 467, 192, 86 (was curious of larger numbers): negligible optimization yields and target not met
- Third optimization returned the two columns; made 5 layers with neurons of 30, 70, 18, 8, 2; cut down epochs to 50 seeing lack of returns past 40 epochs: slight increase in performance but target not met

*Conclusion*
Overall, this model was around 73-74% accurate in predicting the classification problem. Using a model with greater correlation between input and output would likely result in higher prediction accuracy. This could be achieved by doing additional data cleaning up front, as well as using a model with different activation functions and iterating until higher accuracy is reached; one thing of note being to look at the names column as it is very messy. 