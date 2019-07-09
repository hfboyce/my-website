+++
title = "Fresh Prep: Order Predictions"
date = 2019-06-27
draft = false

#Tags: can be used for filtering projects.

#Example: tags = ["machine-learning", "deep-learning"]
#Project summary to display on homepage.

summary = "Predicting future orders for Fresh Prep a Vancouver Local Meal Delivery Company "

#Slides (optional).
#Associate this page with Markdown slides.
#Simply enter your slide deck's filename without extension.
#E.g. slides = "example-slides" references
#content/slides/example-slides.md.
#Otherwise, set slides = "".
slides = ""

#Optional external URL for project (replaces project detail page).
external_link = ""

#Links (optional).

#url_pdf = "" url_code = "" url_dataset = "" url_slides = "" url_video = "" url_poster = ""

url_video = "https://drive.google.com/file/d/1SMXQXHZKUIhUgyqobPEwAn9cb6Mk7lfD/view?usp=sharing"

#Custom links (optional).

#Uncomment line below to enable. For multiple links, use the form [{...}, {...}, {...}].
#url_custom = [{icon_pack = "fab", icon="twitter", name="Follow", url = "https://twitter.com"}]

#Featured image
#To use, add an image named featured.jpg/png to your page's folder.

[image]

#Caption (optional)
caption = ""

#Focal point (optional)
#Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight

focal_point = "Center"
+++

<font size="5"> **Summary:**</font>    
Fresh Prep, a local meal kit delivery company, has been striving to help their busy clientele cook quick, healthy dinners. The business model consists of delivering high quality ingredients and recipes to cook meals in under 30 minutes each week. Ingredients come pre-chopped and pre-portioned for faster cooking. This project explored Fresh Prep's data in an attempt to predict the weekly number of orders. Our team built a model that predicts a probability of ordering for each client, from features that were all engineered and calculated. 

<font size="5"> **Nomenclature and Specifics:**</font>    

Fresh Prep orders can be either:  

- <font color="#7db024"> **Skipped** </font>  - an order that does not get delivered or charged, or    
- <font color="#7db024"> **Billed** </font> - an order which will be delivered and charged to the client.       

From there, a specific customer can choose to set their status to either of the following:  

- <font color="#7db024"> **Active** </font> - orders are automatically billed each week or    
- <font color="#7db024"> **Paused** </font> - orders are automatically skipped each week    

<center><img src="orders.jpg"></center>
  <center><font size="2" color="#A9A9A9"><strong> Fig 1: Examples of billed (left) and skipped (right) orders </strong></font></center>

<font size="5"> **Goal:**</font>     

Our analysis focused around which active clients would be taking an action of opting out of particular orders and paused clients opting in for future orders. 
The question we were attempting to answer for Fresh Prep was approximately **How many orders can the company expect in upcoming weeks?**   
In order to give a better estimate to this question our analysis was concentrated on answering instead **Which customers will be ordering in the upcoming weeks**. 
This enabled Fresh Prep to:

* Target specific clients to improve future order rates
* Improve marketing, production and financial strategies, and
* Avoid sending unnecessary emails to clients who have a larger chance of ordering or not ordering at all. 


<font size="5"> **Procedure:**</font>  



<center><img src="img2.png"></center>
  <center><font size="2" color="#A9A9A9"><strong> Fig 1: From the ColourblindR package, applying theme_trita() </strong></font></center>

<center><img src="img3.png"></center>
  <center><font size="2" color="#A9A9A9"><strong> Fig 2: From the ColourblindR package, applying theme_prota() </strong></font></center>

<center><img src="img4.png"></center>
  <center><font size="2" color="#A9A9A9"><strong> Fig 4: From the Colourblind8 package, using method plot_histogram() </strong></font></center>



