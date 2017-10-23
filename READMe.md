# Udacity Interview Practice for FSND

## Question 1
### What is the most influential book or blog post you’ve read regarding web development?
	In 2014, I learned Ruby on the Rails Development. In the initial phase developing Ruby on the Rainls and coding Ruby codes was tough for me, I searched the best Ruby book in the internet and found one. 

	"Beginining Ruby From Novice to Professional" is my best book ever in my coding life. The book taught me everything about the ruby, installation to running functions and even large stacks of codes. The author Perer Cooper taught me Ruby at all to being proficient and confident enought to develop my own web applications on the rails. I learned enough how to add HTML, CSS, and JavaScript to the Rails. I also learned how to face the coding interviews for the web developer job.

## Question 2
###	Tell me about a web application you have built. Why did you choose to build it? What did you learn? What challenges did you face and how did you overcome them?
	I am volunteering in 211 Sonoma County now. In the past year I developed a website for 211 Sonoma County '211sonoma.org'. It was my great project in my life. I developed a website from scratch to deploy. I am a web developer, while I was looking for a job I contacted volunteer center of Sonoma County and asked them if they have any website project to be done. The introduced me to coordinator of 211 Sonoma County and I started making website. It was challenged job for me and hard to design and code but I did it.

## Question 3
###	Write a function in Python that takes a list of strings and returns a single string that is an HTML unordered list (<ul>...</ul>) of those strings. You should include a brief explanation of your code. Then, what would you have to consider if the original list was provided by user input?

```
python
def unordered_list(strings):
  # creating unordered list tag
  lst = '<ul>'

  # iterate over strings
  for s in strings:
    # append list item tag with contents of one element in strings
    lst += '<li>%s</li>' % s

  # append closing unordered list tag
  lst += '</ul>'
  return lst
```

If the original list is supplied by user input, the function should check if the input is a list, and if the list contains strings.

## Question 4
###	List 2-3 attacks that web applications are vulnerable to. How do these attacks work? How can we prevent those attacks? 
Cross-Site Request Forgery: This type of attack is used in conjunction with social engineering. It allows attackers to trick users into performing actions without their knowledge.For example stealing money from the banking account.

Missing Function Level Access Control: This category covers situations in which higher-privilege functionality is hidden from a lower-privilege or unauthenticated user rather than being enforced through access controls. For example an attack in which a lower-privilege user gains access to the administration interface or a Web application. 

Injection: As the all-time favorite category of application attacks, injections let attackers modify a back-end statement of command through unsanitized user input. For example taking user data and password from the SQL.

## Question 5
###	Here is some starter code for a Flask Web Application. Expand on that and include a route that simulates rolling two dice and returns the result in JSON. You should include a brief explanation of your code.
from flask import Flask
app = Flask(__name__)
import jsonimport random
@app.route('/')
def hello_world():
return 'Hello World!'
if __name__ == '__main__':
app.debug = True
app.run()

```
python
from flask import Flask
app = Flask(__name__)
import json import random
@app.route('/')
def hello_world():
  return 'Hello World!'

# Route takes one argument, the number of sides on the die
@app.route('/roll_dice/<int:sides>/json')
def roll_dice(sides):
  """Return the result of two dice with user-specified number of sides
  being rolled as a json object"""

  # Assign the result of the die roll
  die1 = random.randint(1,sides)
  die2 = random.randint(1,sides)

  # Return the results of the dice rolled as json string, sorted by key
  return json.dumps({'die1': die1, 'die2': die2}, sort_keys=True)

if __name__ == '__main__':
  app.debug = True
  app.run()
```

I've added the functionality to roll two dice and return the result as a json string. 
I've included the ability to pass the number of sides the dice have to the function since it wasn't specified and expands the functionality. 
The result of each die roll is assigned to a variable. The function returns the results of json.dumps(), sorted by key.


## Question 6
### If you were to start your full-stack developer position today, what would be your goals a year from now?
I have almost completed the FUll-Stack Nano Degree. Now I know Full-Stack Web Development with Python backend, JavaScript, HTML, CSS front end and SQL Database. I am not proficient but I know how to develop a full-stack web application. If I am hired today as a full-stack developer I will focus my job, I will use my skills that I learned from Udacity and try to win the employer's satisfaciton. 

I have already applied for the Front-End web developer nanodegree scholorship in the Udacity. If I get chance I will complete the fron-end web development nanodegree and most popular JavaScript framework 'React' nanodegree in next six months. In one year I will be a professional full-stack developer with knowledge of updated and latest techonology. 

## Job Posting
This is the url (https://www.linkedin.com/jobs/view/453227755/) a job that I would like to apply. Here are the responsibilities laid out in the posting.
```
Help build the web based version of WhatsApp in Javascript, HTML5 and CSS3
Work closely with, and incorporate feedback from PMs, designers and other engineers
Pro-actively enhance our web platform
```

