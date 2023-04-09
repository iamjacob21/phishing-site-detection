# Phishing Site URLs Prediction
Phishing Site URLs Prediction is a project that aims to detect and prevent phishing attacks by using machine learning techniques. Phishing attacks are attempts to steal sensitive information such as passwords, credit card numbers, or personal details by impersonating legitimate websites or emails. Phishing Site URLs Prediction uses features of the uniform resource locator (URL) such as the presence of http or https, redirection, length, etc. to classify a website as phishing or legitimate123. This project can help users and organizations to protect themselves from falling victim to phishing scams.
## What is a phishing attack?
Phishing is a type of social engineering attack often used to steal user data, including login credentials and credit card numbers. It occurs when an attacker, masquerading as a trusted entity, dupes a victim into opening an email, instant message, or text message.
## Phishing attack examples
 A spoofed email ostensibly from myuniversity.edu is mass-distributed to as many faculty members as possible. The email claims that the user’s password is about to expire. Instructions are given to go to myuniversity.edu/renewal to renew their password within 24 hours.

![image](https://user-images.githubusercontent.com/126444840/230752220-3bf4b0d7-e3ea-45a2-9e0f-282700e31556.png)

## Several things can occur by clicking the link. For example:

The user is redirected to myuniversity.edurenewal.com, a bogus page appearing exactly like the real renewal page, where both new and existing passwords are requested. The attacker, monitoring the page, hijacks the original password to gain access to secured areas on the university network.

The user is sent to the actual password renewal page. However, while being redirected, a malicious script activates in the background to hijack the user’s session cookie. This results in a reflected XSS attack, giving the perpetrator privileged access to the university network.
## Objective
A phishing website is a common social engineering method that mimics trustful uniform resource locators (URLs) and webpages. The objective of this project is to train machine learning models and deep neural nets on the dataset created to predict phishing websites. Both phishing and benign URLs of websites are gathered to form a dataset and from them required URL and website content-based features are extracted. The performance level of each model is measures and compared.

## Data Collection
The set of phishing URLs are collected from opensource service called **kaggle**. This service provide a set of phishing URLs in format like csv. that gets updated hourly. To download the data: https://www.kaggle.com/taruntiwarihp/phishing-site-urls. From this dataset, 5000 random phishing URLs are collected to train the ML models.

The legitimate URLs are obatined from the open datasets of the University of New Brunswick, https://www.unb.ca/cic/datasets/url-2016.html. This dataset has a collection of benign, spam, phishing, malware & defacement URLs. Out of all these types, the benign url dataset is considered for this project. From this dataset, 5000 random legitimate URLs are collected to train the ML models.
## why ONEAPI ?
 ![image](https://user-images.githubusercontent.com/126444840/230752511-0404836d-6daf-470f-840b-36d7b13c3c13.png)

Using machine learning to detect phishing sites can be computationally expensive, and training and running these algorithms can become increasingly difficult as the amount of data and complexity of models increase. ONEAPI provides developers with a set of tools to optimize and accelerate their code on Intel CPUs, GPUs, and other accelerators. By using ONEAPI to optimize our phishing site detection algorithm, we can significantly speed up the training and testing process, analyze larger datasets, and improve the accuracy of our detection algorithm, ultimately better protecting users from the dangers of online phishing attacks.

## Results & Discussion
The logistics regression and multinomialNB algorithms used in this project achieved an accuracy of 96.36% in predicting phishing sites. This high accuracy suggests that machine learning can be effective in detecting phishing sites. Additionally, by using ONEAPI to optimize the algorithm, we can significantly improve the performance and accuracy of the model also it reduced the overall runtime and GPU usage significantly compared to normal platforms.
