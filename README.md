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
There is a wiki-type website with a search function, an index of topics or categories you can click through, and ideally also some type of search filtering based on various metadata (for example created/modified dates, categories, keywords). At first, the wiki will only be fed with documentation about the system it is supporting. This could be any existing official or unofficial documentation, where the sources are verified by experienced colleagues. 

The main type of page on the wiki will contain the following sections, where information will be submitted manually by colleagues:
1. Issue description
   - Some standard format for issue description, probably similar to that of classic test cases - steps to reproduce, expected outcome, and actual outcome, but with "possible root causes" added
   - "Actual outcome" includes symptoms both from the user perspective, and the more technical perspective, e.g. screenshots, error messages in logs, etc.
2. Solution description
   - Less constrained than the issue description. Will explain the soltion and leave room for explaining why a solution works, pointing back to documentation where one can read more
   - Important follow-up steps. For example, if an error has been causing data issues, how can the data be cleaned up?
   - Artifacts needed for the solution, for example scripts or files 

### Filling data
An AI agent will read the colleagues' submissions and, based to its context documentation, apply the information in the submissions to the formats/templates for a wiki page and create a new page, or merge the information to an existing wiki-page, if the issue is already described. As the wiki grows, the agent will have more information to base future understandings on, and more merges to make - i.e. building the knowledge on some specific problem. Each registered problem/solution will be assigned categories and tags which can later be used in search.

### Searching data
The second main part of this solution is the search function. 
1. There will be a "formal" search possibility, which lets the user filter on categories/tags, dates, etc., for each problem/solution.
2. Furthermore, there will be a "free text search", where the user can chat with an LLM, which will be able to suggest which registered problems/solution might be relevant to what the user is describing. This model will act much more as a search engine than a classic LLM, because we want to avoid hallucinations and irrelevant side tracks.
If no search results are found, the AI in the solution will suggest which of its context documentation might be relevant to go through. 

## Data sources and AI methods
Where does your data come from? Do you collect it yourself or do you use data collected by someone else?
The data source for this project is some selected documentation for the system at hand. This can include public official documentation, e.g. [Microsoft Learn](https://learn.microsoft.com/), and any internal documentation (e.g. .docx files). After the original context is established, new data will be added manually by the users, with the help of the LLM model in the system, which will format and align the data based on the existing context. 

| Syntax               | Description |
| -------------------- | ----------- |
| Public documentation | Obtained online            |
| Internal documentation  | Obtained from developers        |
| Manually input data  | Obtained during live use of the system        |

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
