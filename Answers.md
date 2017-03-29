# How long did you spend on the coding test?
2h 01m 34s since new project creation (except tea breaks)

~2.5 - 3h including tea breaks

and extra ~2-3 hours to unswer all questions

# What would you change / implement in your application given more time?
* __Tests: Full scenario tests (as in AC).__
As far as I understand, you use SpecFlow + Selenium for this, so I should study Selenium )
* __Tests: Controller tests__
I have used DI – but had no time to use it in test
* __Tests: refactoring__, more data, “wrong data” tests
* __UI: Styles__
Unfortunately, I have run out of time, so only simple UI is applied.
It must be scalable, optimized for mobile devices (I hope most users of this service will be mobile users)
* __UI: Validation__
I should add validation messages about wrong input data.
* __UI: Ajax__
Ajax is good, but I should add another (non-ajax) behaviour to cover the situation js is disabled in the browser
* __UI: handle invalid Images__
Investigate and fix the “no image” issue
* __Business: Validation and error handling__
More proper way of xml parsing (++ test different incorrect inputs)
Add valid error pages (I did not change the default one)
* __Common: more layers__
Move different parts of logic to different layers (projects)
For example, 
PicViewerCommon – [Entities] folder
PicViewerBusiness – [Convertors] folder
PicViewerServices – [APIAccess] folder
* __Total code refactoring__
To decrease the dev time I selected one of the MVC templates, I should remove all unnecessary code.
* __Business: MVC__
Move logic of data retrieving from Controller to Model

# Did you use IOC? Please explain your reasons either way.
Yes, I used IOC for service calls.
Reason –write tests without actual calling of services.
But I should refactor it a little bit (to make the ICategoriesService categoriesService not public )

# How would you debug an issue in production code?
It depends on the type of the issue:
* Slow performance – we should measure and improve the performance
* Application crushes with a particular exception – review the exceptions, try to reproduce on dev environment, fix
* Application does not work at all – check prod environment

# What improvements would you make to the cat API?
Category API:
* The cat list should be just http://thecatapi.com/api/categories
* So, no “list” at the end
Images API:
* The link should be http://thecatapi.com/api/categories/dream/images?results_per_page=10
* Name of category moved to another place
* "get" is not required in the link
* As far as I understand format is always xml, so do we really need this parameter?

# What are you two favourite frameworks for .Net?

.NET Core is a brand new framework and I’d like to use it in my future projects.
Even more, may be it is a good idea to re-do this test task on the .NET Core to research it deeply.

And if this question is about favorite tools (Nuget packages), then
* Entity Framework as favorite ORM
* MsTest as favorite unit testing framework (may be, this will changes to SpecFlow soon)
* Knockoutjs as a js tool 

# What is your favourite new feature in .Net?
Unfortunately, I have not found any brand new .Net features (since 4.5) what are related to my everyday work.


# Describe yourself in JSON.
{
  "name": "Vladimir Tataurov",
  "birth": {
	    "day": 3,
	    "month": 4,
      "year": 1984,
	  },
   "gender": "Male",
   "education": {
       "university": {
		"name": "StPetersburg State University",
		"graduation_year": 2000,
		"grade": "Master of computer science"
   },
   "interests": {
       "dancing":[
		“Waltz”,
		“Salsa”,
		“Bachata”
		],
       "sport":[
		“Skiing”,
		“Climbing”
		],
	     "technologies":[
		“.Net”,
		“SQL”,
		“js”
		]
   }
}

