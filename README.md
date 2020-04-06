# COVID-19 Volunteer Database

## Rough Idea and Motivation
* There are people in my community who would love to help with being human subjects in the testing of COVID-19 treatments / studies. I am one such person. I would love to be informed of all current and on-going COVID-19 treatments that are a good fit for my background, and currently the only way I can think of of finding out about these trials is just by going to a database of trials, looking through the inclusion and exclusion criteria, and figuring out if this is a good fit.
* It sounds nice to create a database of volunteers who have expressed interest in being test subjects for these trials, where people will privately post some basic information about themselves, and we will show them the list of trials they may be eligible for, as well as contact information for each trial, and then save their basic (maybe anonymized?) information in case a new study comes along that they are eligible for.
* The data on each trial could, tentatively, come from clinicaltrials.gov - there are probably other repositories collecting trial information specializing in different countries.


## The entire process could look like:

### Onboarding interview
1. New user fills in a survey with some basic health characteristics about themselves (like sex, DOB, whether they are currently exposed to COVID-19 / have it / have had it), what kind of trials they are interested in. Obviously PID should never be shared with anyone else.
2. IF there are current trials they may be eligible for that are recruiting (or maybe also just active?), display a set of results of the studies they are eligible for, with contact information, in an accessible way.
    * Maybe even for each study we could link to an article writeup about the study in question? But that sounds kind of annoying to implement.
    * Figure out what characteristics of each study are interesting to a reader later.
        * This might be a good point on which to ask people more versed in study design / recruiting volunteers what to do here.
    * Accessibility can even just look like, in the UI of the site, making everything look less science-y. Even though clinicaltrials.gov is very good.
    * Important questions for volunteers:
        * Am I eligible? (Some stuff will just be really difficult to develop a survey for)
        * What is the study about - is it observational or is there an intervention being tested? If intervention, what is the intervention?
        * Who do I contact with more information?
    * I would try to make it very easy to reach out to learn more: e.g. maybe even pop up a pre-populated email template to help reach out to the email address listed as a contact, if there is an email listed.
3. After being shown all trials you are potentially eligible for right now, users are asked whether they would like for their PID and contact information to be saved, and to be contacted if / when they are ever eligible in a trial they may be interested in. If yes, save the data, otherwise no need to save.

### After onboarding (for users opting to stay in contact with us)
* Allow for users to update their information (and maybe check in every 14 weeks unless prompted otherwise on whether they have fallen sick)
* Maybe allow people to subscribe to a newsletter on recent listings, which allows for people to share this with their friends and family members who may be eligible.
* If users are potentially eligible for a study, send them an email about it.
    * Be the Match registry / other donor registries seem like a good fit in terms of user engagement and actually just for modelling a database off of in general.


## Questions to answer:
* Is creating a user account necessary?
    * Yes I think, because people should be able to update their information, particularly whether or not they have been exposed to COVID
* Should we show active, not recruiting studies?
    * I think we will know more about studies once we encode some information about each of them
* Fundamental questions:
    * Once we have interested volunteers, what is the best way to go about contacting study researchers? Is there a more systematic way to do this?
    * What are the priorities here? Like who are the priority people to target?


## Some resources:
* https://clinicaltrials.gov/api/gui
    * https://clinicaltrials.gov/api/query/full_studies?expr=coronavirus
    * https://clinicaltrials.gov/api/query/study_fields?expr=heart+attack&fields=NCTId,Condition,BriefTitle