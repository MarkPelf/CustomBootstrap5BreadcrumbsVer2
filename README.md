# Custom Bootstrap 5 Breadcrumbs -Ver 2

Custom Breadcrumbs for Bootstrap 5 framework

***Abstract: We are presenting code (CSS) for custom Bootstrap 5 breadcrumbs. This is an improved version of the previously published article.***

## 1 The need for better Breadcrumbs
Bootstrap 5 framework is coming with very basic Breadcrumbs implementation. I needed something much better, both visually and more functional. Over time, in my applications, I found it very useful to use Breadcrumbs to enable the user to go back to the higher level, after he drills into details on the particular item/object. 
Very important to me was the ability to present TEXT DATA IN TWO ROWS, especially in cases where I am showing some data and ID, like an indication that is the data for some Account, and at the same time providing the Account number. 
I was not satisfied with the solutions I saw on the internet, so I developed my own. 
While the title says this is a “Bootstrap 5” library, it is completely independent of the Bootstrap CSS and only chosen colors were taken from the Bootstrap CSS to align with the Bootstrap 5 theme. You can use it independently from Bootstrap if you like. 
### 1.1	Changes in this version
This version incorporates suggestions and code from Graeme_Grant@codeproject.com to make the code shorter. I do not necessarily agree with all the suggestions, because I think code human readability is more important than shorter code. So, I made my own new version. 
Also, this version uses Bootstrap Icons [1] instead of Font Awesome Icons. 

## 2 Final result
Here is what the final result looks like, together with the demo code that generates it. I created breadcrumbs strips in 3 sizes (large, medium, small), with optional usage of icons. Colors can be chosen at will, and the hover effect is present by default, unless explicitly disabled. The hover effect is usually disabled for the last breadcrumb because that is the current selection in effect. 

![55_pic21](Readme/55_pic21.png)

Here is the HTML code that generates the above rendering. Any web developer should be able to read the HTML code and match it to the above picture to find the variant he/she likes. 
If you want to use icons, you can install the free version of Bootstrap Icons [1], and refer to it, similar to how it is done in this example. HTML code for icon usage is a bit complicated because we needed to separate icons and text into 2 separate elements so they could be styled independently. 

``` js
<!DOCTYPE html>
<html>

<head>
    <link rel="stylesheet" href="breadcrumb3.css" />
    <!-- Download bootstrap icons from https://icons.getbootstrap.com/#install  
        and install -->
    <link rel="stylesheet" href="bootstrap-icons-1.11.3\font\bootstrap-icons.min.css" />
</head>

<body>
    <!--Large size --------------------------------------------------------------->
    <H5>Large size, info case</H5>
    <div class="breadcrumb3-lg ">
        <a href="#" class="breadcrumb3-item info">Accounts</a>
        <a href="#" class="breadcrumb3-item info">Account number</br>123456</a>
        <a href="#" class="breadcrumb3-item primary">Details</a>
    </div>
    <H5>Large size, info case, with no hover effect on the last button</H5>
    <div class="breadcrumb3-lg ">
        <a href="#" class="breadcrumb3-item info">Contracts</a>
        <a href="#" class="breadcrumb3-item info">Contract number</br>99999-2024</a>
        <a href="#" class="breadcrumb3-item primary no-hover-effect">Contract Info</a>
    </div>
    <H5>Large size, Rainbow</H5>
    <div class="breadcrumb3-lg ">
        <a href="#" class="breadcrumb3-item info ">Breadcrumb</br>info</a>
        <a href="#" class="breadcrumb3-item primary ">Breadcrumb</br>primary</a>
        <a href="#" class="breadcrumb3-item warning ">Breadcrumb</br>warning</a>
        <a href="#" class="breadcrumb3-item success ">Breadcrumb</br>success</a>
        <a href="#" class="breadcrumb3-item secondary ">Breadcrumb</br>secondary</a>
        <a href="#" class="breadcrumb3-item light ">Breadcrumb</br>light</a>
        <a href="#" class="breadcrumb3-item danger ">Breadcrumb</br>danger</a>
    </div>
    <H5>Large size, icons usage</H5>
    <div class="breadcrumb3-lg ">
        <a href="#" class="breadcrumb3-item info">
            <span class="breadcrumb3-icon" ><i class="bi bi-people-fill"></i></span> 
            <span class="breadcrumb3-text" >Users</span>
        </a>
        <a href="#" class="breadcrumb3-item info">
            <span class="breadcrumb3-icon" ><i class="bi bi-person-fill"></i></span>
            <span class="breadcrumb3-text" >User number</br>123456</span>
        </a>
        <a href="#" class="breadcrumb3-item primary"> 
            <span class="breadcrumb3-icon" ><i class="bi bi-info-circle-fill"></i></span>
            <span class="breadcrumb3-text" >Details</span>
        </a>
    </div>

    <!--Medium size --------------------------------------------------------------->
    <H5>Medium size, info case</H5>
    <div class="breadcrumb3-md ">
        <a href="#" class="breadcrumb3-item info">Accounts</a>
        <a href="#" class="breadcrumb3-item info">Account number</br>123456</a>
        <a href="#" class="breadcrumb3-item primary">Details</a>
    </div>
    <H5>Medium size, info case, with no hover effect on the last button</H5>
    <div class="breadcrumb3-md ">
        <a href="#" class="breadcrumb3-item info">Contracts</a>
        <a href="#" class="breadcrumb3-item info">Contract number</br>99999-2024</a>
        <a href="#" class="breadcrumb3-item primary no-hover-effect">Contract Info</a>
    </div>
    <H5>Medium size, Rainbow</H5>
    <div class="breadcrumb3-md ">
        <a href="#" class="breadcrumb3-item info ">Breadcrumb</br>info</a>
        <a href="#" class="breadcrumb3-item primary ">Breadcrumb</br>primary</a>
        <a href="#" class="breadcrumb3-item warning ">Breadcrumb</br>warning</a>
        <a href="#" class="breadcrumb3-item success ">Breadcrumb</br>success</a>
        <a href="#" class="breadcrumb3-item secondary ">Breadcrumb</br>secondary</a>
        <a href="#" class="breadcrumb3-item light ">Breadcrumb</br>light</a>
        <a href="#" class="breadcrumb3-item danger ">Breadcrumb</br>danger</a>
    </div>
    <H5>Medium size, icons usage</H5>
    <div class="breadcrumb3-md ">
        <a href="#" class="breadcrumb3-item info">
            <span class="breadcrumb3-icon" ><i class="bi bi-people-fill"></i></span> 
            <span class="breadcrumb3-text" >Users</span>
        </a>
        <a href="#" class="breadcrumb3-item info">
            <span class="breadcrumb3-icon" ><i class="bi bi-person-fill"></i></span>
            <span class="breadcrumb3-text" >User number</br>123456</span>
        </a>
        <a href="#" class="breadcrumb3-item primary"> 
            <span class="breadcrumb3-icon" ><i class="bi bi-info-circle-fill"></i></span>
            <span class="breadcrumb3-text" >Details</span>
        </a>
    </div>

    <!--Small size --------------------------------------------------------------->
    <H5>Small size, info case</H5>
    <div class="breadcrumb3-sm ">
        <a href="#" class="breadcrumb3-item info">Accounts</a>
        <a href="#" class="breadcrumb3-item info">Account number</br>123456</a>
        <a href="#" class="breadcrumb3-item primary">Details</a>
    </div>
    <H5>Small size, info case, with no hover effect on the last button</H5>
    <div class="breadcrumb3-sm  ">
        <a href="#" class="breadcrumb3-item info">Contracts</a>
        <a href="#" class="breadcrumb3-item info">Contract number</br>99999-2024</a>
        <a href="#" class="breadcrumb3-item primary no-hover-effect">Contract Info</a>
    </div>
    <H5>Small size, Rainbow</H5>
    <div class="breadcrumb3-sm  ">
        <a href="#" class="breadcrumb3-item info ">Breadcrumb</br>info</a>
        <a href="#" class="breadcrumb3-item primary ">Breadcrumb</br>primary</a>
        <a href="#" class="breadcrumb3-item warning ">Breadcrumb</br>warning</a>
        <a href="#" class="breadcrumb3-item success ">Breadcrumb</br>success</a>
        <a href="#" class="breadcrumb3-item secondary ">Breadcrumb</br>secondary</a>
        <a href="#" class="breadcrumb3-item light ">Breadcrumb</br>light</a>
        <a href="#" class="breadcrumb3-item danger ">Breadcrumb</br>danger</a>
    </div>
    <H5>Small size, icons usage</H5>
    <div class="breadcrumb3-sm  ">
        <a href="#" class="breadcrumb3-item info">
            <span class="breadcrumb3-icon" ><i class="bi bi-people-fill"></i></span> 
            <span class="breadcrumb3-text" >Users</span>
        </a>
        <a href="#" class="breadcrumb3-item info">
            <span class="breadcrumb3-icon" ><i class="bi bi-person-fill"></i></span>
            <span class="breadcrumb3-text" >User number</br>123456</span>
        </a>
        <a href="#" class="breadcrumb3-item primary"> 
            <span class="breadcrumb3-icon" ><i class="bi bi-info-circle-fill"></i></span>
            <span class="breadcrumb3-text" >Details</span>
        </a>
    </div>
</body>

</html>
``` 

## 3 Breadcrumbs CSS
Here is the CSS, no JavaScript is needed. I deliberately used the class name “breadcrumbs3” to avoid name collision with the Bootstrap 5 original class. 

See ***Breadcrumb3.css*** in the repository. 

4 Full Article
--------------

This is just excerpt from an article published at:
[Custom Bootstrap 5 Breadcrumbs -Ver 2](https://markpelf.com/2114/custom-bootstrap-5-breadcrumbs-ver-2/)

5 References
------------

[1] https://icons.getbootstrap.com/#install  
[2] https://markpelf.com/2114/custom-bootstrap-5-breadcrumbs-ver-2/



