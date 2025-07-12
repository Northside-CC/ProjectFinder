# Project Finder
A place where all of the code and files that we used to setup Project Finder will live to make it easy to share with other churches.
----------
> [!IMPORTANT]
> There is _a lot_ of ways we customized the Sign-Ups feature within our instance of [Rock RMS](https://rockrms.com). This repo is intended to house all of the info pertaining to it, but inevitably it will be customized in a way that doesn't fit your business logic. I'm always happy to help, so reach out on Rocket.chat if you have any questions!

## 👀 See it in action
[Project Finder](https://mynorthside.com/projectfinder)

[Zoom Call Overview](https://vimeo.com/938307929/33358b2b7d?share=copy)

## 🤔 Why did we do it this way?
Historically, we've put a huge focus on community serving one month out of the year (typically in April), and called it **Serve Day** (it's a month, not a day, we know...it's confusing don't judge 🫣). In the months leading up to Serve Day, our local community partners would notify us about projects they needed completed (landscaping, general construction, deep cleaning, etc.). Our local outreach team would organize them so that our community could sign-up for a project and serve.

We made a shift in 2024, thanks to the power of Sign-Ups, to make projects available all year long. We still maintained a large focus on serving in April (which is why you'll see references and logic to Serve Day in the code), but Project Finder itself is evergreen.

### Process
1. Project Submission
   - Our community partners and individuals are the ones who know about the project. And in order for this to scale, our local outreach team couldn't be the only ones creating and overseeing the projects. So there's a form that is sent to someone that gathers all the information needed to create a Sign-Up Opportunity (_i.e. project with shifts_).
2. Project Approval
   - Using Connections, we built an approval process that allowed our local outreach team to approve the project and verify that it had all the necessary pieces of information before publishing. We used an attribute on the Sign-Up group type to indicate whether a project was approved or not.
3. Project Publishing
   - We use the `IsPublic` field of the `Group` model to indicate whether or not a project was published. However, the Sign-Up Finder block doesn't take into account the `IsPublic` field, so you'll us use that logic in the code for the Project Finder.
4. Project Management
   - We wanted to allow the team lead to have as much ownership of the project as possible. So we tapped into what was already available in the Group Toolbox and customized one specifically for Sign-Up project leaders. This toolbox allows them to remove people from the project, see a link to share for others to sign up, and communicate with email / text, among other things.
5. Project Automation
   - We've always found reporting off of archived groups a little difficult, so to keep the Sign-Up Overview list of projects clean, we wrote some workflows to automate the "cleaning up" of these projects. They will self-sort into "previous project" folders by year, so we can easily access projects that have happened in the past without them cluttering the UI.
6. Project Reporting
   - What's a good initiative if you can't measure it? We wrote several KPIs and interfaces for our local outreach team to access insightful info about how Project Finder is going.# ProjectFinder
