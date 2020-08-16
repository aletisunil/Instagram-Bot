# Instagram Bot
Automatically likes the posts of the respective user

  **Prerequisites:**
<ul>
 <li>Selenium</li>
<li>Python</li>
<li>Webdriver</li>
</ul>

Intially, we need selenium to automate, And we can check by executing those commands in your python IDLE or Code Editors
import selenium
print selenium.__version__
Next, we need to install webdriver and you can choose either Google chrome or mozilla firefox webdriver and I gave a link to install Chrome webdriver.

And now let's dig in to the code

**Step 1:**
we need to import webdriver and keys from selenium, these Keys are used to send username and password in input fields.
import sleep from time

**Step 2:**
Create a class which takes username,password and Other user id to whom you want to like the posts
And next you need to locate webdriver and assign to a variable, in my case my webdriver is located in "/Users/Aleti Sunil/Downloads/chromedriver_win32/chromedriver.exe"

**Step 3:**
In order to open Instagram, we need to use driver.get command
And for entering username and password fields, we need to locate the input field by using XPATH, ``` driver.find_element_by_xpath command```
To click on button or any link, we use click() function.

**Step 4:**
After successfull login, we need to drive in to the person's profile to whom we want to like the posts and that can be done by driver.get("https://www.instagram.com/"+OtherUserId)
After going in to user profile, we need to get number of posts so that we can iterate over the posts.

**Step 5:**
we need to pull latest post from the his/her profile by using classname or xpath, I used classname to pull the post
```driver.find_element_by_class_name("_9AhH0")```
To like the posts, we need to get the xpath of that like button
```driver.find_element_by_xpath('/html/body/div[4]/div[2]/div/article/div[2]/section[1]/span[1]/button')```
And to iterate over other posts we need find xpath for "next" button, so that this bot can iterate till last post.

**Step 6:**
You need to enter ur username, password and username of other person to whom you want to like
**Ex:**
```Instabot('abcxcwe','dfasd32963','capdt')#username,password,username of other person```
I added sleep commands so that page gets loaded by the time otherwise an error is thrown.

![Video](InstagramLikingBot.mp4)
