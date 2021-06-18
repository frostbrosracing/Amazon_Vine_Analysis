# Analysis of Amazon Product Review Ratings

## Project Overview of the Analysis
#### The goal of this project was to determine if there is any bias toward favorable reviews from Vine members.  
The Vine Program helps promote customer feedback through reviews of products they are provided by Amazon.  Companies that use Amazon for their distribution pay a fee to Amazon to have their products reviewed.  Amazon provides review information for a wide range of product categories and makes them available through their Amazon Simple Storage Service (Amazon S3).  This analysis was done on a dataset of reviews for the **tool** category.

#### Resources
- Data Source: <p>
`https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Tools_v1_00.tsv.gz`

- Software:  Google Colab, Jupyter Notebook
- Languages: PySpark, Pandas, Python
- Database Resources:  Amazon Web Services (AWS), PostGreSQL, pgAdmin4
  
## Results of the Analysis
* The tools dataset contained over 1.7 million reviews.
* These reviews were given by over 1 million customers for 183,810 unique products.  
1. The dataset was imported into a Google Colab notebook and transformed with Spark DataFrames.
  
![tools_dataset](https://user-images.githubusercontent.com/77071776/122621489-53b67580-d05b-11eb-8314-8decca5cca37.PNG)

2. A customer DataFrame was created which aggregated all their reviews based on their `customer_id` and resulted in 1,053,515 unique customers 
  
![customers_table](https://user-images.githubusercontent.com/77071776/122621533-79dc1580-d05b-11eb-9734-9896dbafb6fa.PNG)

3. A product DataFrame was created with duplicate products dropped.  This resulted in 183,810 products.
  
![products_table](https://user-images.githubusercontent.com/77071776/122622538-a9d8e800-d05e-11eb-9e07-0443a7f8011d.PNG)

4.  A review DataFrame was created with each of the the 1,741,100 reviews. 

![review_id_table](https://user-images.githubusercontent.com/77071776/122622701-28358a00-d05f-11eb-814c-28715db726e7.PNG)


  
  
## Summary
