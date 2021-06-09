# CommonLit-Readability-Prize
Rate the complexity of literary passages for grades 3-12 classroom use

## Description
Can machine learning identify the appropriate reading level of a passage of text, and help inspire learning? Reading is an essential skill for academic success. When students have access to engaging passages offering the right level of challenge, they naturally develop reading skills.

Currently, most educational texts are matched to readers using traditional readability methods or commercially available formulas. However, each has its issues. Tools like Flesch-Kincaid Grade Level are based on weak proxies of text decoding (i.e., characters or syllables per word) and syntactic complexity (i.e., number or words per sentence). As a result, they lack construct and theoretical validity. At the same time, commercially available formulas, such as Lexile, can be cost-prohibitive, lack suitable validation studies, and suffer from transparency issues when the formula's features aren't publicly available.

CommonLit, Inc., is a nonprofit education technology organization serving over 20 million teachers and students with free digital reading and writing lessons for grades 3-12. Together with Georgia State University, an R1 public research university in Atlanta, they are challenging Kagglers to improve readability rating methods.

In this competition, you’ll build algorithms to rate the complexity of reading passages for grade 3-12 classroom use. To accomplish this, you'll pair your machine learning skills with a dataset that includes readers from a wide variety of age groups and a large collection of texts taken from various domains. Winning models will be sure to incorporate text cohesion and semantics.

If successful, you'll aid administrators, teachers, and students. Literacy curriculum developers and teachers who choose passages will be able to quickly and accurately evaluate works for their classrooms. Plus, these formulas will become more accessible for all. Perhaps most importantly, students will benefit from feedback on the complexity and readability of their work, making it far easier to improve essential reading skills.

## Evaluation
Submissions are scored on the root mean squared error. RMSE is defined as:

RMSE=1𝑛∑𝑖=1𝑛(𝑦𝑖−𝑦̂ 𝑖)2
where 𝑦̂  is the predicted value, 𝑦 is the original value, and 𝑛 is the number of rows in the test data.

## Data Description
In this competition, we're predicting the reading ease of excerpts from literature. We've provided excerpts from several time periods and a wide range of reading ease scores. Note that the test set includes a slightly larger proportion of modern texts (the type of texts we want to generalize to) than the training set.

Also note that while licensing information is provided for the public test set (because the associated excerpts are available for display / use), the hidden private test set includes only blank license / legal information.

### Files
train.csv - the training set
test.csv - the test set

### Columns
id - unique ID for excerpt
url_legal - URL of source - this is blank in the test set.
license - license of source material - this is blank in the test set.
excerpt - text to predict reading ease of
target - reading ease
standard_error - measure of spread of scores among multiple raters for each excerpt. Not included for test data.
