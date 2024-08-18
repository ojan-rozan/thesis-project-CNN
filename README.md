# Multi-Label Classification Movie Genre Based on Poster Using InceptionResNetV2 and Xception Architecture

## Project Introduction

<p>This project is an undergraduate thesis aimed at developing an algorithm for multi-label classification of movie genres based on posters using InceptionResNetV2 and Xception. The algorithm will help the streaming platform provide movie recommendations with the correct genres based on their posters.</p>

## Objectives
<ul>
  <li>
    Develop a CNN algorithm for multi-label classification.
  </li>
  <li>
    Compare the performance of two architectures based on accuracy and hamming loss.
  </li>
</ul>

## Dataset
<p>The dataset used is from the IMDb website, which was scraped using Google Colaboratory.</p>

## Methodology
1. Web Scraping
   <ul>
     <li>
       Chrome Driver: Since Google Colaboratory was used, the Chrome Driver was initialized first.
     </li>
     <li>
       Selenium: This package was used for automatically scrolling down the website.
     </li>
     <li>
       BeautifulSoup: This package was used to extract the HTML code from the website.
     </li>
     <li>
       Json: This package was used to retrieve the main code from the website.
     </li>
   </ul>
2. Feature Engineering
   <ul>
     <li>
       Multi-Label Encoding: Convert multi-label genre categories into a binary matrix.
     </li>
     <li>
       Normalization: Normalize the pixel values of the posters.
     </li>
   </ul>
3. Splitting Data
   <ul>
     <li>
       The data was split into 70% training dataset, 20% validation dataset, and 10% testing dataset.
     </li>
   </ul>
4. Multi-Label Random Oversampling
   <ul>
     <li>
       One of the challenges in multi-label classification is an imbalanced dataset. To address this issue, Multi-Label Random Oversampling was used. This method resamples data by duplicating instances of the minority class and was applied only to the training dataset.
     </li>
   </ul>
5. Modeling
   <ul>
     <li>
       Data Augmentation: This technique was used to add more data to the training dataset.
     </li>
     <li>
       InceptionResNetV2 and Xception: These architectures were trained using the resampled training data and the validation dataset, combined with transfer learning.
     </li>
     <li>
       Transfer Learning: This method was used to improve accuracy.
     </li>
   </ul>
6. Evaluation
   <ul>
     <li>
       Hamming Loss: This metric was used to measure the extent of misclassification by the model.
     </li>
     <li>
       Accuracy: This metric was used to assess the overall performance of the model.
     </li>
   </ul>
## The Result
<figure>
    <img src="/Result of Model.png"
         alt="Table Comparison">
	<figcaption><p align="center">Image 1. Tabel Comparison</p></figcaption>
</figure>

<p>
  Based on the image above, it can be concluded that the Xception architecture is the best architecture for multi-label movie genre classification as it has a lower hamming loss and a higher accuracy.
</p>
