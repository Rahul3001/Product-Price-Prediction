# Product-Price-Prediction
A dataset of amazon products.
## Objective 
### To predict the price of the product given Information like:
Image : Containing links to the image of the product
Brand : Containing information about the brand of the product
Title : Text data containing the title of the product page
Specifications : Column which contains the specifications of the product
Highlights : Text data which contains a summary about the product
Rating : Contains the cumulative rating given to that product by the customers
Price : Contains the price of that product. (To be predicted for products which does not have price mentioned)

## Approach :
1) Cleaned and preprocessed the data first.
2) Images are downloaded and a VGG-16 model is applied to extract the bottle neck features.
3) Textual data is combined together using weightage for each text column (Given heighest weightage to title of the product).
4) Combined the extracted features and applied XGBoost on top of the data.
5) Results = r2_score of 0.61 for training data and 0.54 on the test data
