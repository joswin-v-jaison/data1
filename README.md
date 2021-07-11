# data1
## Product recommendation using modcloth dataset
### Approach used is collaborative filtering
Necessary packages like pandas,numpy,matplotlib,seaborn is imported.Data is represented using crosstab to display the tabulation of 2 or more factors.
The dataset include _12_ columns which are:
###  item_id,user_id,rating,timestamp,	size,fit,	user_attr,	model_attr,	category,	brand,	year	,split	
Then a cross  tab is created which display the cross tabulation between model attribute and user attribute column. The columns model_attr and category is concatenated into a single column modcat for effective reccomendation.Then a pivot table is constructed where user_id is displayed in rows,modcat is displayed in columns and ratings in values.
Then the null rating  values are replaced with zero.<br/> 2 approaches can be used .Either cosine similarity or Pearson correlation.Here i have used Pearson correlation.An inbuilt method called corr is used to display the correlation matrix.
## Making recommendations
A list with name of the product[modcat column] and rating is passed to the getsimilar products function which recommends the related products to the customer.The elements are sorted based on ratings in descending order.As a driver code i have passed the 'small and large dress' with rating 5. <br/>
It will display the result as:<br/>
People who bought small and large dress also purchased:<br/>
Small outerwear<br/>
small and large bottoms<br/>
small tops<br/>
small and large tops<br/>
small bottoms<br/>
small and large outerwears<br/>
small dresses


