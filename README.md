# BuildingAI_course_project
Final project for the Building AI course.

## Summary
This is a smart, collaborative, wiki-solution for documenting problems and solutions in a system, intended to be used e.g. by consultants who daily solve problems for clients and users in the system. The solution can also be used to train new hires.

## Background
At my work, we maintain an IT-system for several clients (bug fixing, configuration, changes, general support), and a lot of the troubleshooting we do is repetetive but never documented in a way properly that lets colleagues (especially new ones) benefit from previous findings. Either it is not documented, or it is documented in scattered places. That means we often have to start from scratch, or rely on getting first-hand information from someone who has previously seen the issue at hand. 

Therefore, this project intends to solve the following problems:
* Reliance on outdated, incomplete, scattered, or unclear documentation
* Uncertainty in where to start troubleshooting, especially for newer colleagues
* Stress among colleagues when time is excessively spent on helping newer colleagues, since existing understanding and explanations live mainly in people's heads
* Efficiency in solving issues for clients - higher efficiency would likely result in happier client and more revenue in the long run

## How is it used?
Describe the process of using the solution. In what kind situations is the solution needed (environment, time, etc.)? Who are the users, what kinds of needs should be taken into account?

There is a wiki-type website with a search function, an index of topics or categories you can click through, and ideally also some type of search filtering based on various metadata (for example created/modified dates, categories, keywords). At first, the wiki will only be fed with documentation about the system it is supporting. This could be any existing official or unofficial documentation, where the sources are verified by experienced colleagues. 

The main type of page on the wiki will contain the following sections, where information will be submitted manually by colleagues:
1. Issue description
  2. Some standard format for issue description, probably similar to that of classic test cases - steps to reproduce, expected outcome, and actual outcome, but with "possible root causes" added
  3. "Actual outcome" includes symptoms both from the user perspective, and the more technical perspective, e.g. screenshots, error messages in logs, etc.
4. Solution description
  5. Less constrained than the issue description. Will explain the soltion and leave room for explaining why a solution works, pointing back to documentation where one can read more
  6. Important follow-up steps. For example, if an error has been causing data issues, how can the data be cleaned up?
  7. Artifacts needed for the solution, for example scripts or files 

An AI agent will read the colleagues' submissions and, based to its context documentation, apply the information in the submissions to the formats/templates for a wiki page and create a new page, or merge the information to an existing wiki-page, if the issue is already described. As the wiki grows, the agent will have more information to base future understandings on, and more merges to make - i.e. building the knowledge on some specific problem.



## Data sources and AI methods
Where does your data come from? Do you collect it yourself or do you use data collected by someone else?
If you need to use links, here's an example:
[Twitter API](https://developer.twitter.com/en/docs)

| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |

## Challenges
What does your project _not_ solve? Which limitations and ethical considerations should be taken into account when deploying a solution like this?

- our clients have customized solutions. Some issues might only be relevant for one client. The
- moderation. Still need humans to check every now and then.
- over reliance on this. What if the ai misunderstands?
- regurgitation of incorrectly worded information/input
- bloating on specific wiki pages if issues are too similar but really 2 different things

## What next?
How could your project grow and become something even more? What kind of skills, what kind of assistance would you  need to move on? 


## Acknowledgments
This project is inspired by my colleagues through the years, who have several times wished for a central source of knowledge-sharing. We maintain an IT-system for several clients, and a lot of the troubleshooting we do is repetetive but never documented in a way properly that lets new colleagues benefit from previous findings. That means newcomers often have to start from scratch, and rely on getting 
