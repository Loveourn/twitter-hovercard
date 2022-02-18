# twitter-hovercard
The HTML is very self explanatory and very easy. We create wrappers around and then we create three <div> tags which will contain the content.
  COPY
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Twitter Hovercard</title>
    <link rel="stylesheet" href="./styles.css" />
  </head>
  <body>
    <div class="container">
      <div class="card">
        <div class="profile">
          <div class="main-profile"></div>
          <div class="user-bio"></div>
          <div class="user-follows"></div>
        </div>
      </div>
    </div>
  </body>
</html>
1. main-profile div
The main-profile div will basically contain the Profile Picture, Name, Handle and the Follow button. Which will be in the first row. We will then use flexbox to style it.


COPY

COPY

COPY

COPY
<div class="main-profile">
  <div class="user-info">
    <img src="./profile.jpg" alt="Profile Pic" />
    <h3>Max Programming</h3>
    <p>@MaxProgramming1</p>
  </div>
  <div class="follow-btn">
    <button>Follow</button>
  </div>
</div>
2. user-bio div
This div will contain the bio of the user, in this case my bio. You can separate it into different lines using the <br /> tag.


COPY

COPY

COPY

COPY
<div class="user-bio">
  <p>
    👨‍💻 Programmer, Learner, YTuber, Blogger, and Cricket lover!
    <br />
    😊 15 years old
    <br />
    My name is Usman
    <br />
    ☪ Muslim
    <br />
  
  </p>
</div>
3. user-follows div
This is the simplest one of all. You just create two <div> tags inside it with Following and Followers and their numbers.

We use the <b> tags to bolden out the numbers.


COPY

COPY

COPY

COPY
<div class="user-follows">
  <div><b>613</b> Following</div>
  <div><b>471</b> Followers</div>
</div>
This is what we get after this table is done. Let's now style it out with the magic of CSS.

image.png

🎨 CSS
1. Resets
At the start, we set the margin and padding to 0, and set the box-sizing to border-box. And then we set the font for every element to be sans-serif according to the system.

We style the container to center everything on the page


COPY

COPY

COPY

COPY
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
}

.container {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}
image.png

2. The Card
Now to style the card div, we and add shadow, border radius and padding to it.


COPY

COPY

COPY

COPY
.card {
  box-shadow: 1px 1px 10px 1px #a1a1a1;
  border-radius: 10px;
  padding: 20px;
}
image.png

3. Main Profile
Now as the main-profile contains the main details, we'll position it better using Flexbox.


COPY

COPY

COPY

COPY
.main-profile {
  display: flex;
  justify-content: space-between;
  margin-bottom: 20px;
}
And then we will add some stylings to make the profile picture smaller, increase the size for the name, and change the color of the handle.


COPY

COPY

COPY

COPY
.user-info img {
  width: 100px;
  border-radius: 50%;
}

.user-info h3 {
  font-size: 1.3rem;
}

.user-info p {
  color: #5b7083;
}
This is the progress so far

image.png

Let's style the Follow button now.

Here, we set the border and the text to the twitter blue color, the background is set to the same color but transparent. We make the text bold, and add a hover effect with a transition.


COPY

COPY

COPY

COPY
.follow-btn button {
  font-size: 1.5rem;
  border: 3px solid #1da1f2;
  border-radius: 25px;
  background-color: rgba(29, 161, 242, 0);
  padding: 8px 20px;
  margin: 5px;
  font-weight: bold;
  color: #1da1f2;
  cursor: pointer;
  outline: none;
  transition: all 0.2s ease-in-out;
}

.follow-btn button:hover {
  background-color: rgba(29, 161, 242, 0.2);
}
Now we got the perfect button with the hover effect as well. Which change the background color's opacity.

image.png

4. User bio
The bio is fairly easy. We just change the color of the text, add some margin and change the color of the <a> tags like the styles of Twitter.


COPY

COPY

COPY

COPY
.user-bio {
  color: #0f1419;
  margin-bottom: 10px;
}

.user-bio a {
  color: #1da1f2;
  text-decoration: none;
}

.user-bio a:hover {
  text-decoration: underline;
}
image.png

5. User Follows
This is the easiest part. We use flexbox, we add some margins to the <div>. And we change the color of the text.


COPY

COPY

COPY

COPY
.user-follows {
  display: flex;
  color: #5b7083;
}

.user-follows div {
  margin-right: 10px;
}

.user-follows b {
  color: black;
}
And that is how you recreate Twitter's hover card using HTML and CSS. I hope you like this blog post. If you do, please leave a like comment down below about your experience.

Here's the source code.

GitHub - max-programming/twitter-hovercard
Contribute to max-programming/twitter-hovercard development by creating an account on GitHub.
github.com
Thanks for reading!
