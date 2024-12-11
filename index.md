<h1>CS 499 Capstone</h1>
<h2>Introduction</h2>
My name is Galina Vitvitskaya and I've been working as a Software Developer for close to full 4 years now. I started my journey with self teaching myself html like many back in the day to customize my little online profiles, and soon learned there is way more out there and how interesting it can be. I mainly enjoy working with React first and foremost, but I also have good experience with C# and Java.</p>
<h2>Professional Self-Assessment</h2>
<p></p>Over the course of my education and parallel career I have learned many things, a lot of which admittedly were self-taught but this just helped me be more self-sufficient and resourceful in the fast changing world of software development. During my time at SNHU I've learned a lot more about proper way to build software and how to document my code in a way that people(or me) looking at it in the future aren't going to be completely lost about what is actually being done with it.</p>
<h3>Communication and Collaboration</h3>
<p>I've worked with remote teams in my professional life and learned the importance of quick and reliable communication. It is incredibly important to be able to break down technical jargon to non-technical individuals to understand what the client actually wants in a situation. Defending ones position about certain technical choices is difficult at times but through the different projects during my time in college I learned the way to do so efficiently and with proper technical backing that would explain those decisions.</p>
<h3>Software Engineering and Database</h3>
<p>One of the most helpful courses at SNHU for me was the CS-340, in this course we learned how to build a MongoDB connected application. Previously to this course I've never really worked with MongoDB and haven't had to connect an application to a database by myself. My experience with databases was all SQL based and someone else had set up and connected the database to the application that was developed.</p>
<p>Having this experience now allows me to better understand how to start thinking about database design and use. The follow up course of CS-465 where I actually created a database from scratch and connected to a web app was built upon this previous knowledge.</p>
<h3>Security</h3>
<p>I've also learned some automated testing with JUnit. Unit tests are important as they provide automated testing for functions and allow for errors and unexpected results to be caught early on in the production cycle before the faulty code actually gets merged into the main branch of the project and causes issues down the line.</p>
<p>I've also learned the importance of sanitizing input from users to prevent any SQL injection attacks as well as just verifying that any input that goes into the database is one that the database is actually expecting. CS-465 also taught me how to set up authentication with a JWT token which before I just interacted with from the outside.</p>
<h2>Narratives & Enhancements</h2>
<p>For my final capstone project I've chosen one singular piece of software from my time at SNHU, that being the Travlr Gateway website built in CS-465.</p>
<p>The project was a website built with a MEAN stack, where the "public" facing front end was server with Express and utilized handlebars templating language. The backend was written in Angular. MongoDB was used to store data for the whole website. Initially the only dynamic parts of the "public" site was the travel plans.</p>
<p>I specifically chosen this artifact because I knew that I could do all three enhancements on one project and show how things interact together instead of picking three different items that are unconnected. This also allowed me to manage my time efficiently by working on multiple enhancements at once, and as I'm also currently working full time this was incredibly important to me.</p>
<style>
.project_btn{
    background:#fff6e9;
    padding:10px;
    border-radius:5px;
    border:2px solid #bdb6ad;
}

.project_btn:hover{
    background:#fffbf6;
}
</style>
<div style="display:flex; gap: 10px; justify-content: center;">
<a class="project_btn" href="https://github.com/galinavitsk/SNHU_CS465_C-5">The Original Code</a>
<a class="project_btn" href="https://github.com/galinavitsk/SNHU_CS465_C-5/tree/cs499-software_design_enchancement">The Enhanced Code</a>
<a class="project_btn" href="https://youtu.be/NL67xt9vM-w">Initial Code Review</a>
</div>
</div>
<h3>Enhancement One: Software Design and Engineering </h3>
<p>The first enhancement I quickly rewrote the entirety of the Admin back end from Angular to React. This was primarily done to showcase my knowledge of React as well as provide the much needed UI facelift. I've also added a toast notification system to inform the user when they have been logged out.</p>
<p>The other improvement I've made at this stage was switching from "Code" as the identifier for Trips to using the database generated Ids to update them. "Code" to me felt like an internal company value that the theoretical client might want to change in the future, while ids should never change during the lifetime of the object.</p>
Initially I was planning to implement a full file picker and a jwt refresh process, but then realized that with the use-case of this program this wouldn't actually provide any value and decided to go with a simpler scheme.</p>
<h3>Enhancements Two & Three: Algorithms and Data Structure, and Databases </h3>
<p>While working on the second enhancement I realized it made sense to work on them together so they also get one slot on my narrative here. I've added a new object "Rooms" and allowed the admin to edit/add/delete them. Previously "Trips" object only had the ability to be added or edited, while I was working with the "Rooms" object I also added the ability to delete "Trips" as well. This delete operation was part of the third enhancement but since I was already working with the databases I made sense to do it now.</p>
<p>For the "Rooms" object I've added validation to "Code" and "Names" to prevent duplication.  While "Code" is still an internal identifier and is not used with the actual database search, it should still be unique for that internal company identification. I've also validated the image name to verify that it was actually an image and not some random text.I've also used regex to validate the input of number fields to prevent any text that shouldn't be there from being entered into the database. In real life a lot of the time we want to make it clear to the end user what sort of information is able to be entered in a specific field and one easy way to do so is to prevent entrance of information that should not be there in the first place.</p>
