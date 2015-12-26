---
layout: article
title:  "DataFrames in Julia!"
date:   2015-12-23 19:11:42 +0530
categories: julia
image.thumb: teaser.gif
---


## DataFrames package is required to read any data frame

Install DataFrames Package in Julia

{% highlight julia %}
Pkg.add("DataFrames")
{% endhighlight %}   

    INFO: Installing ArrayViews v0.6.4
    INFO: Installing DataArrays v0.2.20
    INFO: Installing DataFrames v0.6.10
    INFO: Installing Docile v0.5.19
    INFO: Installing GZip v0.2.18
    INFO: Installing Reexport v0.0.3
    INFO: Installing SortingAlgorithms v0.0.6
    INFO: Installing StatsBase v0.7.4
    INFO: Installing StatsFuns v0.2.0
    INFO: Package database updated
    

Declear DataFrames package

{% highlight julia %}
using DataFrames
{% endhighlight %} 
Set Default display size = 10 in IJulia Notebook

{% highlight julia %}
ENV["LINES"] =10
{% endhighlight %} 



    10



##Read data from csv file

{% highlight julia %}
df = readtable("home_data.csv")
{% endhighlight %} 



<table class="data-frame"><tr><th></th><th>id</th><th>date</th><th>price</th><th>bedrooms</th><th>bathrooms</th><th>sqft_living</th><th>sqft_lot</th><th>floors</th><th>waterfront</th><th>view</th><th>condition</th><th>grade</th><th>sqft_above</th><th>sqft_basement</th><th>yr_built</th><th>yr_renovated</th><th>zipcode</th><th>lat</th><th>long</th><th>sqft_living15</th><th>sqft_lot15</th></tr><tr><th>1</th><td>7129300520</td><td>20141013T000000</td><td>221900</td><td>3</td><td>1.0</td><td>1180</td><td>5650</td><td>1.0</td><td>0</td><td>0</td><td>3</td><td>7</td><td>1180</td><td>0</td><td>1955</td><td>0</td><td>98178</td><td>47.5112</td><td>-122.257</td><td>1340</td><td>5650</td></tr><tr><th>2</th><td>6414100192</td><td>20141209T000000</td><td>538000</td><td>3</td><td>2.25</td><td>2570</td><td>7242</td><td>2.0</td><td>0</td><td>0</td><td>3</td><td>7</td><td>2170</td><td>400</td><td>1951</td><td>1991</td><td>98125</td><td>47.721</td><td>-122.319</td><td>1690</td><td>7639</td></tr><tr><th>3</th><td>5631500400</td><td>20150225T000000</td><td>180000</td><td>2</td><td>1.0</td><td>770</td><td>10000</td><td>1.0</td><td>0</td><td>0</td><td>3</td><td>6</td><td>770</td><td>0</td><td>1933</td><td>0</td><td>98028</td><td>47.7379</td><td>-122.233</td><td>2720</td><td>8062</td></tr><tr><th>4</th><td>2487200875</td><td>20141209T000000</td><td>604000</td><td>4</td><td>3.0</td><td>1960</td><td>5000</td><td>1.0</td><td>0</td><td>0</td><td>5</td><td>7</td><td>1050</td><td>910</td><td>1965</td><td>0</td><td>98136</td><td>47.5208</td><td>-122.393</td><td>1360</td><td>5000</td></tr><tr><th>5</th><td>1954400510</td><td>20150218T000000</td><td>510000</td><td>3</td><td>2.0</td><td>1680</td><td>8080</td><td>1.0</td><td>0</td><td>0</td><td>3</td><td>8</td><td>1680</td><td>0</td><td>1987</td><td>0</td><td>98074</td><td>47.6168</td><td>-122.045</td><td>1800</td><td>7503</td></tr><tr><th>6</th><td>7237550310</td><td>20140512T000000</td><td>1225000</td><td>4</td><td>4.5</td><td>5420</td><td>101930</td><td>1.0</td><td>0</td><td>0</td><td>3</td><td>11</td><td>3890</td><td>1530</td><td>2001</td><td>0</td><td>98053</td><td>47.6561</td><td>-122.005</td><td>4760</td><td>101930</td></tr><tr><th>7</th><td>1321400060</td><td>20140627T000000</td><td>257500</td><td>3</td><td>2.25</td><td>1715</td><td>6819</td><td>2.0</td><td>0</td><td>0</td><td>3</td><td>7</td><td>1715</td><td>0</td><td>1995</td><td>0</td><td>98003</td><td>47.3097</td><td>-122.327</td><td>2238</td><td>6819</td></tr><tr><th>8</th><td>2008000270</td><td>20150115T000000</td><td>291850</td><td>3</td><td>1.5</td><td>1060</td><td>9711</td><td>1.0</td><td>0</td><td>0</td><td>3</td><td>7</td><td>1060</td><td>0</td><td>1963</td><td>0</td><td>98198</td><td>47.4095</td><td>-122.315</td><td>1650</td><td>9711</td></tr><tr><th>9</th><td>2414600126</td><td>20150415T000000</td><td>229500</td><td>3</td><td>1.0</td><td>1780</td><td>7470</td><td>1.0</td><td>0</td><td>0</td><td>3</td><td>7</td><td>1050</td><td>730</td><td>1960</td><td>0</td><td>98146</td><td>47.5123</td><td>-122.337</td><td>1780</td><td>8113</td></tr><tr><th>10</th><td>3793500160</td><td>20150312T000000</td><td>323000</td><td>3</td><td>2.5</td><td>1890</td><td>6560</td><td>2.0</td><td>0</td><td>0</td><td>3</td><td>7</td><td>1890</td><td>0</td><td>2003</td><td>0</td><td>98038</td><td>47.3684</td><td>-122.031</td><td>2390</td><td>7570</td></tr><tr><th>&vellip;</th><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td></tr></table>



### Print the column names

{% highlight julia %}
a = names(df);
println(" Column names : ", a)
{% endhighlight %} 
     Column names : [:id,:date,:price,:bedrooms,:bathrooms,:sqft_living,:sqft_lot,:floors,:waterfront,:view,:condition,:grade,:sqft_above,:sqft_basement,:yr_built,:yr_renovated,:zipcode,:lat,:long,:sqft_living15,:sqft_lot15]
    

###Print top 6 rows of the DataFrame

{% highlight julia %}
head(df)
{% endhighlight %} 



<table class="data-frame"><tr><th></th><th>id</th><th>date</th><th>price</th><th>bedrooms</th><th>bathrooms</th><th>sqft_living</th><th>sqft_lot</th><th>floors</th><th>waterfront</th><th>view</th><th>condition</th><th>grade</th><th>sqft_above</th><th>sqft_basement</th><th>yr_built</th><th>yr_renovated</th><th>zipcode</th><th>lat</th><th>long</th><th>sqft_living15</th><th>sqft_lot15</th></tr><tr><th>1</th><td>7129300520</td><td>20141013T000000</td><td>221900</td><td>3</td><td>1.0</td><td>1180</td><td>5650</td><td>1.0</td><td>0</td><td>0</td><td>3</td><td>7</td><td>1180</td><td>0</td><td>1955</td><td>0</td><td>98178</td><td>47.5112</td><td>-122.257</td><td>1340</td><td>5650</td></tr><tr><th>2</th><td>6414100192</td><td>20141209T000000</td><td>538000</td><td>3</td><td>2.25</td><td>2570</td><td>7242</td><td>2.0</td><td>0</td><td>0</td><td>3</td><td>7</td><td>2170</td><td>400</td><td>1951</td><td>1991</td><td>98125</td><td>47.721</td><td>-122.319</td><td>1690</td><td>7639</td></tr><tr><th>3</th><td>5631500400</td><td>20150225T000000</td><td>180000</td><td>2</td><td>1.0</td><td>770</td><td>10000</td><td>1.0</td><td>0</td><td>0</td><td>3</td><td>6</td><td>770</td><td>0</td><td>1933</td><td>0</td><td>98028</td><td>47.7379</td><td>-122.233</td><td>2720</td><td>8062</td></tr><tr><th>4</th><td>2487200875</td><td>20141209T000000</td><td>604000</td><td>4</td><td>3.0</td><td>1960</td><td>5000</td><td>1.0</td><td>0</td><td>0</td><td>5</td><td>7</td><td>1050</td><td>910</td><td>1965</td><td>0</td><td>98136</td><td>47.5208</td><td>-122.393</td><td>1360</td><td>5000</td></tr><tr><th>5</th><td>1954400510</td><td>20150218T000000</td><td>510000</td><td>3</td><td>2.0</td><td>1680</td><td>8080</td><td>1.0</td><td>0</td><td>0</td><td>3</td><td>8</td><td>1680</td><td>0</td><td>1987</td><td>0</td><td>98074</td><td>47.6168</td><td>-122.045</td><td>1800</td><td>7503</td></tr><tr><th>6</th><td>7237550310</td><td>20140512T000000</td><td>1225000</td><td>4</td><td>4.5</td><td>5420</td><td>101930</td><td>1.0</td><td>0</td><td>0</td><td>3</td><td>11</td><td>3890</td><td>1530</td><td>2001</td><td>0</td><td>98053</td><td>47.6561</td><td>-122.005</td><td>4760</td><td>101930</td></tr></table>



###Print bottom 6 rows of the DataFrame

{% highlight julia %}
tail(df)
{% endhighlight %} 



<table class="data-frame"><tr><th></th><th>id</th><th>date</th><th>price</th><th>bedrooms</th><th>bathrooms</th><th>sqft_living</th><th>sqft_lot</th><th>floors</th><th>waterfront</th><th>view</th><th>condition</th><th>grade</th><th>sqft_above</th><th>sqft_basement</th><th>yr_built</th><th>yr_renovated</th><th>zipcode</th><th>lat</th><th>long</th><th>sqft_living15</th><th>sqft_lot15</th></tr><tr><th>1</th><td>2997800021</td><td>20150219T000000</td><td>475000</td><td>3</td><td>2.5</td><td>1310</td><td>1294</td><td>2.0</td><td>0</td><td>0</td><td>3</td><td>8</td><td>1180</td><td>130</td><td>2008</td><td>0</td><td>98116</td><td>47.5773</td><td>-122.409</td><td>1330</td><td>1265</td></tr><tr><th>2</th><td>263000018</td><td>20140521T000000</td><td>360000</td><td>3</td><td>2.5</td><td>1530</td><td>1131</td><td>3.0</td><td>0</td><td>0</td><td>3</td><td>8</td><td>1530</td><td>0</td><td>2009</td><td>0</td><td>98103</td><td>47.6993</td><td>-122.346</td><td>1530</td><td>1509</td></tr><tr><th>3</th><td>6600060120</td><td>20150223T000000</td><td>400000</td><td>4</td><td>2.5</td><td>2310</td><td>5813</td><td>2.0</td><td>0</td><td>0</td><td>3</td><td>8</td><td>2310</td><td>0</td><td>2014</td><td>0</td><td>98146</td><td>47.5107</td><td>-122.362</td><td>1830</td><td>7200</td></tr><tr><th>4</th><td>1523300141</td><td>20140623T000000</td><td>402101</td><td>2</td><td>0.75</td><td>1020</td><td>1350</td><td>2.0</td><td>0</td><td>0</td><td>3</td><td>7</td><td>1020</td><td>0</td><td>2009</td><td>0</td><td>98144</td><td>47.5944</td><td>-122.299</td><td>1020</td><td>2007</td></tr><tr><th>5</th><td>291310100</td><td>20150116T000000</td><td>400000</td><td>3</td><td>2.5</td><td>1600</td><td>2388</td><td>2.0</td><td>0</td><td>0</td><td>3</td><td>8</td><td>1600</td><td>0</td><td>2004</td><td>0</td><td>98027</td><td>47.5345</td><td>-122.069</td><td>1410</td><td>1287</td></tr><tr><th>6</th><td>1523300157</td><td>20141015T000000</td><td>325000</td><td>2</td><td>0.75</td><td>1020</td><td>1076</td><td>2.0</td><td>0</td><td>0</td><td>3</td><td>7</td><td>1020</td><td>0</td><td>2008</td><td>0</td><td>98144</td><td>47.5941</td><td>-122.299</td><td>1020</td><td>1357</td></tr></table>



###Find the dimension of DataFrame

{% highlight julia %}
size(df)
{% endhighlight %} 



    (21613,21)



size prints DataFrame  df has 21613 rows and 21 columns

###Summarize the total number of bedrooms in the dataset

{% highlight julia %}
describe(df[:bedrooms])
{% endhighlight %} 
    Summary Stats:
    Mean:         3.370842
    Minimum:      0.000000
    1st Quartile: 3.000000
    Median:       3.000000
    3rd Quartile: 4.000000
    Maximum:      33.000000
    

###Find the mean value of price in the dataset

{% highlight julia %}
mean(df[:price])
{% endhighlight %} 



    540088.1419053348



###Find the median value of sqft_living

{% highlight julia %}
median(df[:sqft_living])
{% endhighlight %} 



    1910.0



### Remove id 

{% highlight julia %}
df2 = delete!(df,:id);
head(df2)
{% endhighlight %} 



<table class="data-frame"><tr><th></th><th>date</th><th>price</th><th>bedrooms</th><th>bathrooms</th><th>sqft_living</th><th>sqft_lot</th><th>floors</th><th>waterfront</th><th>view</th><th>condition</th><th>grade</th><th>sqft_above</th><th>sqft_basement</th><th>yr_built</th><th>yr_renovated</th><th>zipcode</th><th>lat</th><th>long</th><th>sqft_living15</th><th>sqft_lot15</th></tr><tr><th>1</th><td>20141013T000000</td><td>221900</td><td>3</td><td>1.0</td><td>1180</td><td>5650</td><td>1.0</td><td>0</td><td>0</td><td>3</td><td>7</td><td>1180</td><td>0</td><td>1955</td><td>0</td><td>98178</td><td>47.5112</td><td>-122.257</td><td>1340</td><td>5650</td></tr><tr><th>2</th><td>20141209T000000</td><td>538000</td><td>3</td><td>2.25</td><td>2570</td><td>7242</td><td>2.0</td><td>0</td><td>0</td><td>3</td><td>7</td><td>2170</td><td>400</td><td>1951</td><td>1991</td><td>98125</td><td>47.721</td><td>-122.319</td><td>1690</td><td>7639</td></tr><tr><th>3</th><td>20150225T000000</td><td>180000</td><td>2</td><td>1.0</td><td>770</td><td>10000</td><td>1.0</td><td>0</td><td>0</td><td>3</td><td>6</td><td>770</td><td>0</td><td>1933</td><td>0</td><td>98028</td><td>47.7379</td><td>-122.233</td><td>2720</td><td>8062</td></tr><tr><th>4</th><td>20141209T000000</td><td>604000</td><td>4</td><td>3.0</td><td>1960</td><td>5000</td><td>1.0</td><td>0</td><td>0</td><td>5</td><td>7</td><td>1050</td><td>910</td><td>1965</td><td>0</td><td>98136</td><td>47.5208</td><td>-122.393</td><td>1360</td><td>5000</td></tr><tr><th>5</th><td>20150218T000000</td><td>510000</td><td>3</td><td>2.0</td><td>1680</td><td>8080</td><td>1.0</td><td>0</td><td>0</td><td>3</td><td>8</td><td>1680</td><td>0</td><td>1987</td><td>0</td><td>98074</td><td>47.6168</td><td>-122.045</td><td>1800</td><td>7503</td></tr><tr><th>6</th><td>20140512T000000</td><td>1225000</td><td>4</td><td>4.5</td><td>5420</td><td>101930</td><td>1.0</td><td>0</td><td>0</td><td>3</td><td>11</td><td>3890</td><td>1530</td><td>2001</td><td>0</td><td>98053</td><td>47.6561</td><td>-122.005</td><td>4760</td><td>101930</td></tr></table>



###Subset data for house with 2 bedrooms

{% highlight julia %}
twoBedroom_data = df[df[:bedrooms] .== 2,:]

{% endhighlight %} 


<table class="data-frame"><tr><th></th><th>id</th><th>date</th><th>price</th><th>bedrooms</th><th>bathrooms</th><th>sqft_living</th><th>sqft_lot</th><th>floors</th><th>waterfront</th><th>view</th><th>condition</th><th>grade</th><th>sqft_above</th><th>sqft_basement</th><th>yr_built</th><th>yr_renovated</th><th>zipcode</th><th>lat</th><th>long</th><th>sqft_living15</th><th>sqft_lot15</th></tr><tr><th>1</th><td>5631500400</td><td>20150225T000000</td><td>180000</td><td>2</td><td>1.0</td><td>770</td><td>10000</td><td>1.0</td><td>0</td><td>0</td><td>3</td><td>6</td><td>770</td><td>0</td><td>1933</td><td>0</td><td>98028</td><td>47.7379</td><td>-122.233</td><td>2720</td><td>8062</td></tr><tr><th>2</th><td>9212900260</td><td>20140527T000000</td><td>468000</td><td>2</td><td>1.0</td><td>1160</td><td>6000</td><td>1.0</td><td>0</td><td>0</td><td>4</td><td>7</td><td>860</td><td>300</td><td>1942</td><td>0</td><td>98115</td><td>47.69</td><td>-122.292</td><td>1330</td><td>6000</td></tr><tr><th>3</th><td>16000397</td><td>20141205T000000</td><td>189000</td><td>2</td><td>1.0</td><td>1200</td><td>9850</td><td>1.0</td><td>0</td><td>0</td><td>4</td><td>7</td><td>1200</td><td>0</td><td>1921</td><td>0</td><td>98002</td><td>47.3089</td><td>-122.21</td><td>1060</td><td>5095</td></tr><tr><th>4</th><td>8091400200</td><td>20140516T000000</td><td>252700</td><td>2</td><td>1.5</td><td>1070</td><td>9643</td><td>1.0</td><td>0</td><td>0</td><td>3</td><td>7</td><td>1070</td><td>0</td><td>1985</td><td>0</td><td>98030</td><td>47.3533</td><td>-122.166</td><td>1220</td><td>8386</td></tr><tr><th>5</th><td>2426039314</td><td>20141201T000000</td><td>280000</td><td>2</td><td>1.5</td><td>1190</td><td>1265</td><td>3.0</td><td>0</td><td>0</td><td>3</td><td>7</td><td>1190</td><td>0</td><td>2005</td><td>0</td><td>98133</td><td>47.7274</td><td>-122.357</td><td>1390</td><td>1756</td></tr><tr><th>6</th><td>3626039271</td><td>20150205T000000</td><td>585000</td><td>2</td><td>1.75</td><td>1980</td><td>8550</td><td>1.0</td><td>0</td><td>0</td><td>3</td><td>7</td><td>990</td><td>990</td><td>1981</td><td>0</td><td>98117</td><td>47.6989</td><td>-122.369</td><td>1480</td><td>6738</td></tr><tr><th>7</th><td>9418400240</td><td>20141028T000000</td><td>355000</td><td>2</td><td>1.0</td><td>2020</td><td>6720</td><td>1.0</td><td>0</td><td>0</td><td>3</td><td>7</td><td>1010</td><td>1010</td><td>1948</td><td>0</td><td>98118</td><td>47.5474</td><td>-122.291</td><td>1720</td><td>6720</td></tr><tr><th>8</th><td>1332700270</td><td>20140519T000000</td><td>215000</td><td>2</td><td>2.25</td><td>1610</td><td>2040</td><td>2.0</td><td>0</td><td>0</td><td>4</td><td>7</td><td>1610</td><td>0</td><td>1979</td><td>0</td><td>98056</td><td>47.518</td><td>-122.194</td><td>1950</td><td>2025</td></tr><tr><th>9</th><td>3869900162</td><td>20140904T000000</td><td>335000</td><td>2</td><td>1.75</td><td>1030</td><td>1066</td><td>2.0</td><td>0</td><td>0</td><td>3</td><td>7</td><td>765</td><td>265</td><td>2006</td><td>0</td><td>98136</td><td>47.5394</td><td>-122.387</td><td>1030</td><td>1106</td></tr><tr><th>10</th><td>3530510041</td><td>20140723T000000</td><td>188500</td><td>2</td><td>1.75</td><td>1240</td><td>2493</td><td>1.0</td><td>0</td><td>0</td><td>4</td><td>8</td><td>1240</td><td>0</td><td>1985</td><td>0</td><td>98198</td><td>47.3813</td><td>-122.322</td><td>1270</td><td>4966</td></tr><tr><th>&vellip;</th><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td></tr></table>



Important point to note here is julia requires elementwise operations for subsetting "." [dot] is required for elementwise operations.

{% highlight julia %}
size(twoBedroom_data)
{% endhighlight %} 



    (2760,21)



There are 2760 houses with 2 bedrooms

###Subset the data for house with 2 bedrooms and sqft_living more than 1000

{% highlight julia %}
twoBedrooms_1000_sqft = df[(df[:bedrooms].== 2).*(df[:sqft_living] .>= 1000),:]
{% endhighlight %} 



<table class="data-frame"><tr><th></th><th>id</th><th>date</th><th>price</th><th>bedrooms</th><th>bathrooms</th><th>sqft_living</th><th>sqft_lot</th><th>floors</th><th>waterfront</th><th>view</th><th>condition</th><th>grade</th><th>sqft_above</th><th>sqft_basement</th><th>yr_built</th><th>yr_renovated</th><th>zipcode</th><th>lat</th><th>long</th><th>sqft_living15</th><th>sqft_lot15</th></tr><tr><th>1</th><td>9212900260</td><td>20140527T000000</td><td>468000</td><td>2</td><td>1.0</td><td>1160</td><td>6000</td><td>1.0</td><td>0</td><td>0</td><td>4</td><td>7</td><td>860</td><td>300</td><td>1942</td><td>0</td><td>98115</td><td>47.69</td><td>-122.292</td><td>1330</td><td>6000</td></tr><tr><th>2</th><td>16000397</td><td>20141205T000000</td><td>189000</td><td>2</td><td>1.0</td><td>1200</td><td>9850</td><td>1.0</td><td>0</td><td>0</td><td>4</td><td>7</td><td>1200</td><td>0</td><td>1921</td><td>0</td><td>98002</td><td>47.3089</td><td>-122.21</td><td>1060</td><td>5095</td></tr><tr><th>3</th><td>8091400200</td><td>20140516T000000</td><td>252700</td><td>2</td><td>1.5</td><td>1070</td><td>9643</td><td>1.0</td><td>0</td><td>0</td><td>3</td><td>7</td><td>1070</td><td>0</td><td>1985</td><td>0</td><td>98030</td><td>47.3533</td><td>-122.166</td><td>1220</td><td>8386</td></tr><tr><th>4</th><td>2426039314</td><td>20141201T000000</td><td>280000</td><td>2</td><td>1.5</td><td>1190</td><td>1265</td><td>3.0</td><td>0</td><td>0</td><td>3</td><td>7</td><td>1190</td><td>0</td><td>2005</td><td>0</td><td>98133</td><td>47.7274</td><td>-122.357</td><td>1390</td><td>1756</td></tr><tr><th>5</th><td>3626039271</td><td>20150205T000000</td><td>585000</td><td>2</td><td>1.75</td><td>1980</td><td>8550</td><td>1.0</td><td>0</td><td>0</td><td>3</td><td>7</td><td>990</td><td>990</td><td>1981</td><td>0</td><td>98117</td><td>47.6989</td><td>-122.369</td><td>1480</td><td>6738</td></tr><tr><th>6</th><td>9418400240</td><td>20141028T000000</td><td>355000</td><td>2</td><td>1.0</td><td>2020</td><td>6720</td><td>1.0</td><td>0</td><td>0</td><td>3</td><td>7</td><td>1010</td><td>1010</td><td>1948</td><td>0</td><td>98118</td><td>47.5474</td><td>-122.291</td><td>1720</td><td>6720</td></tr><tr><th>7</th><td>1332700270</td><td>20140519T000000</td><td>215000</td><td>2</td><td>2.25</td><td>1610</td><td>2040</td><td>2.0</td><td>0</td><td>0</td><td>4</td><td>7</td><td>1610</td><td>0</td><td>1979</td><td>0</td><td>98056</td><td>47.518</td><td>-122.194</td><td>1950</td><td>2025</td></tr><tr><th>8</th><td>3869900162</td><td>20140904T000000</td><td>335000</td><td>2</td><td>1.75</td><td>1030</td><td>1066</td><td>2.0</td><td>0</td><td>0</td><td>3</td><td>7</td><td>765</td><td>265</td><td>2006</td><td>0</td><td>98136</td><td>47.5394</td><td>-122.387</td><td>1030</td><td>1106</td></tr><tr><th>9</th><td>3530510041</td><td>20140723T000000</td><td>188500</td><td>2</td><td>1.75</td><td>1240</td><td>2493</td><td>1.0</td><td>0</td><td>0</td><td>4</td><td>8</td><td>1240</td><td>0</td><td>1985</td><td>0</td><td>98198</td><td>47.3813</td><td>-122.322</td><td>1270</td><td>4966</td></tr><tr><th>10</th><td>3992700335</td><td>20140707T000000</td><td>382500</td><td>2</td><td>1.0</td><td>1190</td><td>4440</td><td>1.0</td><td>0</td><td>0</td><td>3</td><td>6</td><td>1190</td><td>0</td><td>1981</td><td>0</td><td>98125</td><td>47.7135</td><td>-122.287</td><td>1060</td><td>5715</td></tr><tr><th>&vellip;</th><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td></tr></table>



{% highlight julia %}
size(twoBedrooms_1000_sqft)

{% endhighlight %} 


    (1824,21)



There are 1824 houses with 2 bedrooms with sqft_living more than 1000 sqft

### Sort the dataset according to the increasing order of price 

{% highlight julia %}
sorted_data = sort(df,cols = :price)
{% endhighlight %} 



<table class="data-frame"><tr><th></th><th>id</th><th>date</th><th>price</th><th>bedrooms</th><th>bathrooms</th><th>sqft_living</th><th>sqft_lot</th><th>floors</th><th>waterfront</th><th>view</th><th>condition</th><th>grade</th><th>sqft_above</th><th>sqft_basement</th><th>yr_built</th><th>yr_renovated</th><th>zipcode</th><th>lat</th><th>long</th><th>sqft_living15</th><th>sqft_lot15</th></tr><tr><th>1</th><td>3421079032</td><td>20150217T000000</td><td>75000</td><td>1</td><td>0.0</td><td>670</td><td>43377</td><td>1.0</td><td>0</td><td>0</td><td>3</td><td>3</td><td>670</td><td>0</td><td>1966</td><td>0</td><td>98022</td><td>47.2638</td><td>-121.906</td><td>1160</td><td>42882</td></tr><tr><th>2</th><td>40000362</td><td>20140506T000000</td><td>78000</td><td>2</td><td>1.0</td><td>780</td><td>16344</td><td>1.0</td><td>0</td><td>0</td><td>1</td><td>5</td><td>780</td><td>0</td><td>1942</td><td>0</td><td>98168</td><td>47.4739</td><td>-122.28</td><td>1700</td><td>10387</td></tr><tr><th>3</th><td>8658300340</td><td>20140523T000000</td><td>80000</td><td>1</td><td>0.75</td><td>430</td><td>5050</td><td>1.0</td><td>0</td><td>0</td><td>2</td><td>4</td><td>430</td><td>0</td><td>1912</td><td>0</td><td>98014</td><td>47.6499</td><td>-121.909</td><td>1200</td><td>7500</td></tr><tr><th>4</th><td>3028200080</td><td>20150324T000000</td><td>81000</td><td>2</td><td>1.0</td><td>730</td><td>9975</td><td>1.0</td><td>0</td><td>0</td><td>1</td><td>5</td><td>730</td><td>0</td><td>1943</td><td>0</td><td>98168</td><td>47.4808</td><td>-122.315</td><td>860</td><td>9000</td></tr><tr><th>5</th><td>3883800011</td><td>20141105T000000</td><td>82000</td><td>3</td><td>1.0</td><td>860</td><td>10426</td><td>1.0</td><td>0</td><td>0</td><td>3</td><td>6</td><td>860</td><td>0</td><td>1954</td><td>0</td><td>98146</td><td>47.4987</td><td>-122.341</td><td>1140</td><td>11250</td></tr><tr><th>6</th><td>1623049041</td><td>20140508T000000</td><td>82500</td><td>2</td><td>1.0</td><td>520</td><td>22334</td><td>1.0</td><td>0</td><td>0</td><td>2</td><td>5</td><td>520</td><td>0</td><td>1951</td><td>0</td><td>98168</td><td>47.4799</td><td>-122.296</td><td>1572</td><td>10570</td></tr><tr><th>7</th><td>7999600180</td><td>20140529T000000</td><td>83000</td><td>2</td><td>1.0</td><td>900</td><td>8580</td><td>1.0</td><td>0</td><td>0</td><td>3</td><td>5</td><td>900</td><td>0</td><td>1918</td><td>0</td><td>98168</td><td>47.4727</td><td>-122.27</td><td>2060</td><td>6533</td></tr><tr><th>8</th><td>1523049188</td><td>20150430T000000</td><td>84000</td><td>2</td><td>1.0</td><td>700</td><td>20130</td><td>1.0</td><td>0</td><td>0</td><td>3</td><td>6</td><td>700</td><td>0</td><td>1949</td><td>0</td><td>98168</td><td>47.4752</td><td>-122.271</td><td>1490</td><td>18630</td></tr><tr><th>9</th><td>2422049104</td><td>20140915T000000</td><td>85000</td><td>2</td><td>1.0</td><td>830</td><td>9000</td><td>1.0</td><td>0</td><td>0</td><td>3</td><td>6</td><td>830</td><td>0</td><td>1939</td><td>0</td><td>98032</td><td>47.3813</td><td>-122.243</td><td>1160</td><td>7680</td></tr><tr><th>10</th><td>1322049150</td><td>20150305T000000</td><td>85000</td><td>2</td><td>1.0</td><td>910</td><td>9753</td><td>1.0</td><td>0</td><td>0</td><td>3</td><td>5</td><td>910</td><td>0</td><td>1947</td><td>0</td><td>98032</td><td>47.3897</td><td>-122.236</td><td>1160</td><td>7405</td></tr><tr><th>&vellip;</th><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td></tr></table>



### Order the dataset in decreasing order of house prices

{% highlight julia %}
sorted_df_2 = sort(df,cols = :price, rev = true)
{% endhighlight %} 



<table class="data-frame"><tr><th></th><th>id</th><th>date</th><th>price</th><th>bedrooms</th><th>bathrooms</th><th>sqft_living</th><th>sqft_lot</th><th>floors</th><th>waterfront</th><th>view</th><th>condition</th><th>grade</th><th>sqft_above</th><th>sqft_basement</th><th>yr_built</th><th>yr_renovated</th><th>zipcode</th><th>lat</th><th>long</th><th>sqft_living15</th><th>sqft_lot15</th></tr><tr><th>1</th><td>6762700020</td><td>20141013T000000</td><td>7700000</td><td>6</td><td>8.0</td><td>12050</td><td>27600</td><td>2.5</td><td>0</td><td>3</td><td>4</td><td>13</td><td>8570</td><td>3480</td><td>1910</td><td>1987</td><td>98102</td><td>47.6298</td><td>-122.323</td><td>3940</td><td>8800</td></tr><tr><th>2</th><td>9808700762</td><td>20140611T000000</td><td>7062500</td><td>5</td><td>4.5</td><td>10040</td><td>37325</td><td>2.0</td><td>1</td><td>2</td><td>3</td><td>11</td><td>7680</td><td>2360</td><td>1940</td><td>2001</td><td>98004</td><td>47.65</td><td>-122.214</td><td>3930</td><td>25449</td></tr><tr><th>3</th><td>9208900037</td><td>20140919T000000</td><td>6885000</td><td>6</td><td>7.75</td><td>9890</td><td>31374</td><td>2.0</td><td>0</td><td>4</td><td>3</td><td>13</td><td>8860</td><td>1030</td><td>2001</td><td>0</td><td>98039</td><td>47.6305</td><td>-122.24</td><td>4540</td><td>42730</td></tr><tr><th>4</th><td>2470100110</td><td>20140804T000000</td><td>5570000</td><td>5</td><td>5.75</td><td>9200</td><td>35069</td><td>2.0</td><td>0</td><td>0</td><td>3</td><td>13</td><td>6200</td><td>3000</td><td>2001</td><td>0</td><td>98039</td><td>47.6289</td><td>-122.233</td><td>3560</td><td>24345</td></tr><tr><th>5</th><td>8907500070</td><td>20150413T000000</td><td>5350000</td><td>5</td><td>5.0</td><td>8000</td><td>23985</td><td>2.0</td><td>0</td><td>4</td><td>3</td><td>12</td><td>6720</td><td>1280</td><td>2009</td><td>0</td><td>98004</td><td>47.6232</td><td>-122.22</td><td>4600</td><td>21750</td></tr><tr><th>6</th><td>7558700030</td><td>20150413T000000</td><td>5300000</td><td>6</td><td>6.0</td><td>7390</td><td>24829</td><td>2.0</td><td>1</td><td>4</td><td>4</td><td>12</td><td>5000</td><td>2390</td><td>1991</td><td>0</td><td>98040</td><td>47.5631</td><td>-122.21</td><td>4320</td><td>24619</td></tr><tr><th>7</th><td>1247600105</td><td>20141020T000000</td><td>5110800</td><td>5</td><td>5.25</td><td>8010</td><td>45517</td><td>2.0</td><td>1</td><td>4</td><td>3</td><td>12</td><td>5990</td><td>2020</td><td>1999</td><td>0</td><td>98033</td><td>47.6767</td><td>-122.211</td><td>3430</td><td>26788</td></tr><tr><th>8</th><td>1924059029</td><td>20140617T000000</td><td>4668000</td><td>5</td><td>6.75</td><td>9640</td><td>13068</td><td>1.0</td><td>1</td><td>4</td><td>3</td><td>12</td><td>4820</td><td>4820</td><td>1983</td><td>2009</td><td>98040</td><td>47.557</td><td>-122.21</td><td>3270</td><td>10454</td></tr><tr><th>9</th><td>7738500731</td><td>20140815T000000</td><td>4500000</td><td>5</td><td>5.5</td><td>6640</td><td>40014</td><td>2.0</td><td>1</td><td>4</td><td>3</td><td>12</td><td>6350</td><td>290</td><td>2004</td><td>0</td><td>98155</td><td>47.7493</td><td>-122.28</td><td>3030</td><td>23408</td></tr><tr><th>10</th><td>3835500195</td><td>20140618T000000</td><td>4489000</td><td>4</td><td>3.0</td><td>6430</td><td>27517</td><td>2.0</td><td>0</td><td>0</td><td>3</td><td>12</td><td>6430</td><td>0</td><td>2001</td><td>0</td><td>98004</td><td>47.6208</td><td>-122.219</td><td>3720</td><td>14592</td></tr><tr><th>&vellip;</th><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td></tr></table>



## Multi level sorting

### Sort house data according to the increasing order of bedrooms and price

{% highlight julia %}
Dual_levelsort = sort(df,cols = [:bedrooms,:price])
{% endhighlight %} 



<table class="data-frame"><tr><th></th><th>id</th><th>date</th><th>price</th><th>bedrooms</th><th>bathrooms</th><th>sqft_living</th><th>sqft_lot</th><th>floors</th><th>waterfront</th><th>view</th><th>condition</th><th>grade</th><th>sqft_above</th><th>sqft_basement</th><th>yr_built</th><th>yr_renovated</th><th>zipcode</th><th>lat</th><th>long</th><th>sqft_living15</th><th>sqft_lot15</th></tr><tr><th>1</th><td>9543000205</td><td>20150413T000000</td><td>139950</td><td>0</td><td>0.0</td><td>844</td><td>4269</td><td>1.0</td><td>0</td><td>0</td><td>4</td><td>7</td><td>844</td><td>0</td><td>1913</td><td>0</td><td>98001</td><td>47.2781</td><td>-122.25</td><td>1380</td><td>9600</td></tr><tr><th>2</th><td>3980300371</td><td>20140926T000000</td><td>142000</td><td>0</td><td>0.0</td><td>290</td><td>20875</td><td>1.0</td><td>0</td><td>0</td><td>1</td><td>1</td><td>290</td><td>0</td><td>1963</td><td>0</td><td>98024</td><td>47.5308</td><td>-121.888</td><td>1620</td><td>22850</td></tr><tr><th>3</th><td>6896300380</td><td>20141002T000000</td><td>228000</td><td>0</td><td>1.0</td><td>390</td><td>5900</td><td>1.0</td><td>0</td><td>0</td><td>2</td><td>4</td><td>390</td><td>0</td><td>1953</td><td>0</td><td>98118</td><td>47.526</td><td>-122.261</td><td>2170</td><td>6000</td></tr><tr><th>4</th><td>7849202190</td><td>20141223T000000</td><td>235000</td><td>0</td><td>0.0</td><td>1470</td><td>4800</td><td>2.0</td><td>0</td><td>0</td><td>3</td><td>7</td><td>1470</td><td>0</td><td>1996</td><td>0</td><td>98065</td><td>47.5265</td><td>-121.828</td><td>1060</td><td>7200</td></tr><tr><th>5</th><td>2310060040</td><td>20140925T000000</td><td>240000</td><td>0</td><td>2.5</td><td>1810</td><td>5669</td><td>2.0</td><td>0</td><td>0</td><td>3</td><td>7</td><td>1810</td><td>0</td><td>2003</td><td>0</td><td>98038</td><td>47.3493</td><td>-122.053</td><td>1810</td><td>5685</td></tr><tr><th>6</th><td>1222029077</td><td>20141029T000000</td><td>265000</td><td>0</td><td>0.75</td><td>384</td><td>213444</td><td>1.0</td><td>0</td><td>0</td><td>3</td><td>4</td><td>384</td><td>0</td><td>2003</td><td>0</td><td>98070</td><td>47.4177</td><td>-122.491</td><td>1920</td><td>224341</td></tr><tr><th>7</th><td>1453602309</td><td>20140805T000000</td><td>288000</td><td>0</td><td>1.5</td><td>1430</td><td>1650</td><td>3.0</td><td>0</td><td>0</td><td>3</td><td>7</td><td>1430</td><td>0</td><td>1999</td><td>0</td><td>98125</td><td>47.7222</td><td>-122.29</td><td>1430</td><td>1650</td></tr><tr><th>8</th><td>7849202299</td><td>20150218T000000</td><td>320000</td><td>0</td><td>2.5</td><td>1490</td><td>7111</td><td>2.0</td><td>0</td><td>0</td><td>3</td><td>7</td><td>1490</td><td>0</td><td>1999</td><td>0</td><td>98065</td><td>47.5261</td><td>-121.826</td><td>1500</td><td>4675</td></tr><tr><th>9</th><td>2569500210</td><td>20141117T000000</td><td>339950</td><td>0</td><td>2.5</td><td>2290</td><td>8319</td><td>2.0</td><td>0</td><td>0</td><td>3</td><td>8</td><td>2290</td><td>0</td><td>1985</td><td>0</td><td>98042</td><td>47.3473</td><td>-122.151</td><td>2500</td><td>8751</td></tr><tr><th>10</th><td>3374500520</td><td>20150429T000000</td><td>355000</td><td>0</td><td>0.0</td><td>2460</td><td>8049</td><td>2.0</td><td>0</td><td>0</td><td>3</td><td>8</td><td>2460</td><td>0</td><td>1990</td><td>0</td><td>98031</td><td>47.4095</td><td>-122.168</td><td>2520</td><td>8050</td></tr><tr><th>&vellip;</th><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td></tr></table>



### Sort data in decreasing order of bedroom and increasing order of price

{% highlight julia %}
dual_sort_2 = sort(df,cols = [:bedrooms,:price],rev = [true,false])
{% endhighlight %} 



<table class="data-frame"><tr><th></th><th>id</th><th>date</th><th>price</th><th>bedrooms</th><th>bathrooms</th><th>sqft_living</th><th>sqft_lot</th><th>floors</th><th>waterfront</th><th>view</th><th>condition</th><th>grade</th><th>sqft_above</th><th>sqft_basement</th><th>yr_built</th><th>yr_renovated</th><th>zipcode</th><th>lat</th><th>long</th><th>sqft_living15</th><th>sqft_lot15</th></tr><tr><th>1</th><td>2402100895</td><td>20140625T000000</td><td>640000</td><td>33</td><td>1.75</td><td>1620</td><td>6000</td><td>1.0</td><td>0</td><td>0</td><td>5</td><td>7</td><td>1040</td><td>580</td><td>1947</td><td>0</td><td>98103</td><td>47.6878</td><td>-122.331</td><td>1330</td><td>4700</td></tr><tr><th>2</th><td>1773100755</td><td>20140821T000000</td><td>520000</td><td>11</td><td>3.0</td><td>3000</td><td>4960</td><td>2.0</td><td>0</td><td>0</td><td>3</td><td>7</td><td>2400</td><td>600</td><td>1918</td><td>1999</td><td>98106</td><td>47.556</td><td>-122.363</td><td>1420</td><td>4960</td></tr><tr><th>3</th><td>5566100170</td><td>20141029T000000</td><td>650000</td><td>10</td><td>2.0</td><td>3610</td><td>11914</td><td>2.0</td><td>0</td><td>0</td><td>4</td><td>7</td><td>3010</td><td>600</td><td>1958</td><td>0</td><td>98006</td><td>47.5705</td><td>-122.175</td><td>2040</td><td>11914</td></tr><tr><th>4</th><td>8812401450</td><td>20141229T000000</td><td>660000</td><td>10</td><td>3.0</td><td>2920</td><td>3745</td><td>2.0</td><td>0</td><td>0</td><td>4</td><td>7</td><td>1860</td><td>1060</td><td>1913</td><td>0</td><td>98105</td><td>47.6635</td><td>-122.32</td><td>1810</td><td>3745</td></tr><tr><th>5</th><td>627300145</td><td>20140814T000000</td><td>1148000</td><td>10</td><td>5.25</td><td>4590</td><td>10920</td><td>1.0</td><td>0</td><td>2</td><td>3</td><td>9</td><td>2500</td><td>2090</td><td>2008</td><td>0</td><td>98004</td><td>47.5861</td><td>-122.113</td><td>2730</td><td>10400</td></tr><tr><th>6</th><td>424049043</td><td>20140811T000000</td><td>450000</td><td>9</td><td>7.5</td><td>4050</td><td>6504</td><td>2.0</td><td>0</td><td>0</td><td>3</td><td>7</td><td>4050</td><td>0</td><td>1996</td><td>0</td><td>98144</td><td>47.5923</td><td>-122.301</td><td>1448</td><td>3866</td></tr><tr><th>7</th><td>1997200215</td><td>20140507T000000</td><td>599999</td><td>9</td><td>4.5</td><td>3830</td><td>6988</td><td>2.5</td><td>0</td><td>0</td><td>3</td><td>7</td><td>2450</td><td>1380</td><td>1938</td><td>0</td><td>98103</td><td>47.6927</td><td>-122.338</td><td>1460</td><td>6291</td></tr><tr><th>8</th><td>2902200015</td><td>20150106T000000</td><td>700000</td><td>9</td><td>3.0</td><td>3680</td><td>4400</td><td>2.0</td><td>0</td><td>0</td><td>3</td><td>7</td><td>2830</td><td>850</td><td>1908</td><td>0</td><td>98102</td><td>47.6374</td><td>-122.324</td><td>1960</td><td>2450</td></tr><tr><th>9</th><td>8823901445</td><td>20150313T000000</td><td>934000</td><td>9</td><td>3.0</td><td>2820</td><td>4480</td><td>2.0</td><td>0</td><td>0</td><td>3</td><td>7</td><td>1880</td><td>940</td><td>1918</td><td>0</td><td>98105</td><td>47.6654</td><td>-122.307</td><td>2460</td><td>4400</td></tr><tr><th>10</th><td>9822700190</td><td>20140808T000000</td><td>1280000</td><td>9</td><td>4.5</td><td>3650</td><td>5000</td><td>2.0</td><td>0</td><td>0</td><td>3</td><td>8</td><td>2530</td><td>1120</td><td>1915</td><td>2010</td><td>98105</td><td>47.6604</td><td>-122.289</td><td>2510</td><td>5000</td></tr><tr><th>&vellip;</th><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td><td>&vellip;</td></tr></table>



### Print the total number of houses available in each zipcode

{% highlight julia %}
Size_by_Zip = by(df,:zipcode,size);
head(Size_by_Zip)
{% endhighlight %} 



<table class="data-frame"><tr><th></th><th>zipcode</th><th>x1</th></tr><tr><th>1</th><td>98001</td><td>(362,20)</td></tr><tr><th>2</th><td>98002</td><td>(199,20)</td></tr><tr><th>3</th><td>98003</td><td>(280,20)</td></tr><tr><th>4</th><td>98004</td><td>(317,20)</td></tr><tr><th>5</th><td>98005</td><td>(168,20)</td></tr><tr><th>6</th><td>98006</td><td>(498,20)</td></tr></table>



Note: The DataFrames package supports the Split-Apply-Combine strategy through the by function, which takes in three arguments: (1) a DataFrame, (2) a column to split the DataFrame on, and (3) a function or expression to apply to each subset of the DataFrame.

### Print maximum price of house in all zipcode

{% highlight julia %}
maxPrice_Zipcode = by(df,:zipcode, testdf -> testdf[indmax(testdf[:price]),[:price]]);
head(maxPrice_Zipcode)
{% endhighlight %} 



<table class="data-frame"><tr><th></th><th>zipcode</th><th>price</th></tr><tr><th>1</th><td>98001</td><td>850000</td></tr><tr><th>2</th><td>98002</td><td>389000</td></tr><tr><th>3</th><td>98003</td><td>950000</td></tr><tr><th>4</th><td>98004</td><td>7062500</td></tr><tr><th>5</th><td>98005</td><td>1960000</td></tr><tr><th>6</th><td>98006</td><td>4208000</td></tr></table>



### Print minimun price of house in all zipcode

{% highlight julia %}
minPrice_Zipcode = by(df,:zipcode, testdf -> testdf[indmin(testdf[:price]),[:price]]);
head(minPrice_Zipcode)
{% endhighlight %} 



<table class="data-frame"><tr><th></th><th>zipcode</th><th>price</th></tr><tr><th>1</th><td>98001</td><td>100000</td></tr><tr><th>2</th><td>98002</td><td>95000</td></tr><tr><th>3</th><td>98003</td><td>128000</td></tr><tr><th>4</th><td>98004</td><td>425000</td></tr><tr><th>5</th><td>98005</td><td>400000</td></tr><tr><th>6</th><td>98006</td><td>247500</td></tr></table>




    
