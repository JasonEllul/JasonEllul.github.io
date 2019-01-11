---
layout: page
title: Projects
---

<!--<div class="uk-card uk-card-default uk-card-small uk-card-body">
<div class="uk-card-media-top uk-height-large uk-cover-container">
<div class="uk-cover" style="width: 100%">
<img src="https://raw.githubusercontent.com/JasonEllul/JasonEllul.github.io/master/public/images/motive_banner.png" alt="Motive Logo Banner">
</div>
</div>    
<p>Motive is a map-based social network I created where users can ... coming soon exclusively to iOS.</p>
</div>-->

<div class="uk-card uk-card-default">
<div class="uk-card-media-top">
<img class="notrounded" src="https://raw.githubusercontent.com/JasonEllul/JasonEllul.github.io/master/public/images/motive_banner.png" alt="Motive Logo Banner">
</div>
<center><h4 class="paddington"><br>Motive is a map-based social network I founded where users can post annotations onto a global map in the form of <i>motives</i>. You can follow an account to view all of their recent motives on your map and then "go" to the post (equivalent of liking a post) as well as add comments.</h4></center>

<img class="notrounded half" src="https://raw.githubusercontent.com/JasonEllul/JasonEllul.github.io/master/public/images/motive_phones.png" alt="Motive Application Running on Phone">

<center><p class="paddington">Here are a few screenshots of the app running on an iPhone. The left screenshot contains an image of the home map, where you view all of the Motives loaded from your feed on a map. You can press on any of the annotations to see more details about the Motive such as comments, distance from you, nearest address, and who's going. The right screenshot is what the feed looks like; where you can see posts in a tablular view as well as filter between your follower's recent Motives or explore public posts. Pressing any Motive in the table will bring you to the location of that Motive on the home map.</p></center>

<br>
<img class="notrounded reducedWidth" src="https://raw.githubusercontent.com/JasonEllul/JasonEllul.github.io/master/public/images/motive_profile.PNG" alt="Motive Profile">
<center><p class="paddington">Above is a screenshot of what a user's profile looks like. This is where you can see someone's posted Motives, as well as the Motives they are going to. You can customize your own profile to your liking by changing your profile picture, display name, username, and banner point location. If you set your profile to private then people will need to request to follow you and view your posts.</p></center>

<h3 class="uk-card-title" style="padding-left: 4%; padding-right: 4%;">How It's Made</h3>
<p class="paddington">It all started with me wishing that there was an app I could open on my phone that would show what's going on around me. Despite having all of these social media apps on my phone, there was nothing that enabled me to simply look at a map and see events being posted. I then had the revelation that I'm a software engineer and could make this app a reality myself!
<br><br>
I began by sketching out what the app would look like and creating the branding. I choose the name Motive because it's catchy, simple, and has a memorable punchline that inspire users to create posts: <i>"What's the Motive?"</i>. I used the site <a href="https://uigradients.com">uigradients.com</a> to find a colour gradient I liked that would suit the app. I choose orange because it accurately portrays the fast paced nature of a social network that shows the user what is currently going on around them. I took design inspiration from SnapChat's SnapMap feature for the map component of the app and Twitter for the text feed. </p>

<img class="notrounded half" src="https://raw.githubusercontent.com/JasonEllul/JasonEllul.github.io/master/public/images/motive_design.png" alt="Motive Design Iterations">

<center><p class="paddington">Here are one of the early sketches I created for a view that would show the details of a specific post. On the right shows what that same functionality ended up looking like in the app.</p></center>
<br>

<img class="notrounded half" src="https://raw.githubusercontent.com/JasonEllul/JasonEllul.github.io/master/public/images/motive_map_compare.png" alt="Motive Design Iterations">

<center><p class="paddington">The home map view after many usability tests and visual overhauls. The home map view originally used the native iOS MapKit and the annotations to represent posts were non-customizable flags. I changed the map to MapBox because the map tiles looked much more aesthetically pleasing and because iOS MapKit did not contain the map camera/ fly functionality I needed for the home map to animate smoothly. Usability testing the previous version of the app determined that I should simplify the tabs of my tab bar controller. I compensated for this by adding a sliding sidebar menu that contains paths to all of the features accessible from the removed tabs.</p></center>
<br>

<img class="notrounded half" src="https://raw.githubusercontent.com/JasonEllul/JasonEllul.github.io/master/public/images/motive_profile_compare.png" alt="Motive Design Iterations">
<center><p class="paddington">The profile view after a few design iterations. I took inspiration from Twitter's profile view for the segmented control styling and the top banner layout. Motive originally had a friend request system, but I changed this to a follower/ following system because this made a lot more sense for how you would use the app. Think about it, it would be much more preferrable to simply just follow someone rather than wait for them to accept your friend request. This becomes especially true when you consider accounts owned by an organization, or accounts that would post where things like sales are. The only upside of a friend request system would be more user privacy and permissions, so I set up an optional privacy system where users can change their settings so that they first need to approve anyone that follows them.</p></center>
<br>
<p class="paddington">The front-end of Motive is made of roughly ~10000 lines of swift split between 40+ classes. The reason why there is so many lines of code is because I did most of the UI programmatically rather than using storyboard, and there are a total of 18 different view controllers so far in the app. The back-end of Motive is powered by Firebase, Google Cloud Functions, and Node.js. I use Firebase Database to store all of the information about the users and posts, and Firebase Storage to store pictures uploaded to the app. I choose to use Firebase for this project because it was easy to implement into my project and it has great realtime database functionality. The only downside is how limited Firebase's query capabilities are, which caused me to have to re-work some features I had originally designed for the app. I use Google Cloud Functions mainly to create optimization in my cloud database and reduce the amount the user needs to download. For example, I programmed multiple cloud functions that calculate the number of children in a collection and return that number to the user. This is useful so the user can simply make an https call to get the amount of people going to a motive rather than downloading every single user ID that is going and counting how many there are. This is effective in reducing Firebase Database costs, cell phone network usage, and overhead battery usage.</p>

<p class="paddington"><br>Motive is coming to the exclusively on the Apple App Store in 2019. It is currently in open beta and you can download the app onto any iOS device <a href="https://testflight.apple.com/join/bNDtFSKZ">here</a>.</p>



<div class="uk-card-body"></div>

</div>

The rest of this page is currently a work in progress as I finish developing Motive... stay tuned for updates!

