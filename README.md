# Capstone_1

## House Prices - Basic Regression Techniques

## Context
### Dataset source : https://www.kaggle.com/datasets/ahmedshahriarsakib/usa-real-estate-dataset
### According to the source of the dataset provided:
#### This dataset contains Real Estate listings in the US broken by State and zip code.

## Business Understanding
### Objective
#### The objective is to find a model that will predict house prices.  This goal will change as the characteristics of the data provided are explored.

#### Many of the features in the dataset provided for this project are described in the "Data Understanding".  We can leverage and tweak them to find the best model.  The initial focus will be to build a codebase that can be leveraged with modifications afterwards.

## Data Understanding

### Data Descriptions
#### Here is the preliminary info about our dataset.
RangeIndex: 1401066 entries, 0 to 1401065
Data columns (total 10 columns):
 #   Column          Non-Null Count    Dtype  
---  ------          --------------    -----  
 0   status          1401066 non-null  object 
 1   bed             1184538 non-null  float64
 2   bath            1206853 non-null  float64
 3   acre_lot        1043599 non-null  float64
 4   city            1400875 non-null  object 
 5   state           1401066 non-null  object 
 6   zip_code        1400587 non-null  float64
 7   house_size      950954 non-null   float64
 8   prev_sold_date  714773 non-null   object 
 9   price           1400958 non-null  float64
dtypes: float64(6), object(4)
memory usage: 106.9+ MB



#### Here is the a list of descriptions for the features in the dataset.
status (Housing status - a. ready for sale or b. ready to build)
bed (# of beds)
bath (# of bathrooms)
acre_lot (Property / Land size in acres)
city (city name)
state (state name)
zip_code (postal code of the area)
house_size (house area/size/living space in square feet)
prev_sold_date (Previously sold date)
price (Housing price, it is either the current listing price or recently sold price if the house is sold recently)

#### For the purpose of this project a macro level analysis will be conducted at the state level for Connecticut, Massachusetts, NJ, NY, and Pennsylvania.
#### The initial count of houses in each state indicate a sufficient number to provide an adequate range.
#### However after removing duplicate entries this may prove to be a bigger challenge when we try micro level analysis.  But we will continue with this approach for Capstone 1.
<table>
<tr>
<th>Before removing duplicates</th>
<th>After removing duplicates</th>
</tr>
<tr>
<td>
state              Count<br/>
<b>Connecticut        98816</b><br/>
Delaware            2135<br/>
Georgia               50<br/>
Louisiana              3<br/>
Maine              36650<br/>
<b>Massachusetts     177170</b><br/>
New Hampshire      51394<br/>
<b>New Jersey        256551</b><br/>
<b>New York          653061</b><br/>
<b>Pennsylvania       20060</b><br/>
Puerto Rico        24679<br/>
Rhode Island       29610<br/>
South Carolina        25<br/>
Tennessee             20<br/>
Vermont            48230<br/>
Virgin Islands      2573<br/>
Virginia              31<br/>
West Virginia          5<br/>
Wyoming                3<br/>
</td>
<td>
state             Count<br/>
<b>Connecticut       13753</b><br/>
Delaware           1290<br/>
Georgia               5<br/>
Louisiana             1<br/>
Maine              4938<br/>
<b>Massachusetts     10051</b><br/>
New Hampshire      3431<br/>
<b>New Jersey        32601</b><br/>
<b>New York          67159</b><br/>
<b>Pennsylvania       9549</b><br/>
Puerto Rico        2645<br/>
Rhode Island       3332<br/>
South Carolina        1<br/>
Tennessee             1<br/>
Vermont            2544<br/>
Virgin Islands      730<br/>
Virginia              7<br/>
West Virginia         1<br/>
Wyoming               1<br/>
</td>
</tr>
</table>


### Model Comparisons
#### Various feature selectors were used with different models.
<table>
<tr><th>Models</th><th>Feature Selectors</th></tr>
<tr><td>Decision Tree</td><td></td></tr>
<tr><td></td><td>Best Parameters</td></tr>
<tr><td></td><td>Recursive Feature Elimination</td></tr>
<tr><td></td><td>Sequential Feature Selector</td></tr>
<tr><td>K-Nearest Neighbors</td><td></td></tr>
<tr><td></td><td>Best Parameters</td></tr>
<tr><td></td><td>Sequential Feature Selector</td></tr>
<tr><td>Lasso</td><td></td></tr>
<tr><td></td><td>Best Parameters</td></tr>
<tr><td></td><td>Select From Model</td></tr>
<tr><td></td><td>Recursive Feature Elimination</td></tr>
<tr><td></td><td>Sequential Feature Selector</td></tr>
<tr><td>Linear and Polynomial</td><td></td></tr>
<tr><td></td><td>Best Parameters</td></tr>
<tr><td></td><td>Select From Model</td></tr>
<tr><td></td><td>Recursive Feature Elimination</td></tr>
<tr><td></td><td>Sequential Feature Selector</td></tr>
<tr><td>Ridge</td><td></td></tr>
<tr><td></td><td>Best Parameters</td></tr>
<tr><td></td><td>Select From Model</td></tr>
<tr><td></td><td>Recursive Feature Elimination</td></tr>
<tr><td></td><td>Sequential Feature Selector</td></tr>
</table>