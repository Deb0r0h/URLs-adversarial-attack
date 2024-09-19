# Adversarial attack

The purpose of this experiment is to test a simple adversary attack and demonstrate its effectiveness by applying it to phishing detection on URLs.

The knowledge is White-box (very ideal case)

Given a neural network for classifying legitimate and phishing URLs, the attack is to slightly modify the URLs so that the network does not classify them correctly

For more details regarding attacks under URL and phishing detection, read the dedicated section 4.2.1 in the PDF

The dataset is like:

| URL                                        | Label |
|--------------------------------------------|-------|
| http://legit.com                    | 0     |
| http://phishing.com          | 1     |

(ask me for the csv file)

The adversarial_attack function applies an adversarial attack to URLs to check the robustness of the classification model:
- transforms the URLs into numerical vectors using a TF-IDF vectorizer.
- introduces small perturbations to the original vectors to try to confound the model.
- predicts whether the modified URLs are phishing or legitimate, returning the new predictions.

