Notes about the FRESCA standard
================================

These are notes-to-self about the FRESH resume standard.  They lay out some of the implicit logic of the schema as I understand it.

# Sections

##Objects

These are structured sections.

### name
>name as it should appear on the resume.

Required.

### meta
>metadata information for the resume, including the resume version, schema, and any other fields required by tools.

Not for use by humans


## Fixed fields
These sections organize some standard, single-item information.

### info
>basic summary information for the candidate, including an optional label or job title, candidate photo, summary, and quote.

field | description
--- | --- | ---
label | A label for this resume, such as 'Full-Stack Developer'.
class | Profession type or 'character class'.
image | URL or path to your picture in JPEG, PNG, GIF, or BMP format.
brief | A short description or summary of yourself as a candidate.
quote | Candidate quote or byline.


### disposition
>overall attitude towards new employment opportunities including: travel, relocation, schedule, desired type of work, and the like.

Info for hiring.  Mostly fixed fields with a few lists (e.g. list of locations willing to work)

field | description
--- | --- | ---
travel | Percentage of time willing to travel (0 to 100).
authorization | Work authorization: citizen, work visa, etc.
commitment | Types of work commitment desired: contract, perm, seasonal, etc.
remote | Open to remote employment opportunities.
relocation | Pairs of locations & willingness to relocate there


### contact
>The 'contact' section contains the candidate's contact information, including phone numbers, emails, websites, IMs, and custom contact types.

Fixed fields + section for other forms of contact.

field | description
--- | --- | ---
email | Primary contact email.
phone | Primary phone number.
website | Website, blog, or home page.
other | list of other contact methods

### location
>The 'location' section, when present, contains the candidate's location and address info.

field | description
--- | --- | ---
address | Your full postal address.
code | Postal or other official routing code.
city | Your home city.
country | Two-digit country code (US, AU, UK, IN, etc.).
region | Your state, region, or province.


## History + Summary
These sections contain a `history` array plus a `summary` string.  The fields for the elements of `history` are shown

### employment
> formal employment history.

field | description
--- | --- | ---
employer | Employer name.
position | Your position or formal job title.
url | Employer website.
start | Date you began work, in YYYY, YYYY-MM, or YYYY-MM-DD format.
end | Date you finished work, in YYYY, YYYY-MM, or YYYY-MM-DD format.
summary | A summary of your achievements and responsibilities under this employer.
highlights | Noteworthy achievements and/or highlights.
location | Freeform location of the job or position, e.g., 'San Francisco, CA' or 'Tokyo'.
keywords | Keywords associated with this position.

### service
> overall service history in the true sense of the word 'service': volunteer work, military participation, civilian core, rescue and emergency services, and the like.

field | description
--- | --- | ---
category | The type of service work, such as volunteer or military.
organization | The service organization, such as Red Cross or National Guard.
position | Your position or formal service role.
url | Organization website.
start | Date you joined the organization, in YYYY, YYYY-MM, or YYYY-MM-DD format.
end | Date you left the organization, in YYYY, YYYY-MM, or YYYY-MM-DD format.
summary | A summary of your achievements and responsibilities at this organization.
highlights | Noteworthy achievements and/or highlights.
keywords | Keywords associated with this service.
location | Freeform location of the position, e.g., 'San Francisco, CA' or 'Tokyo'.


### education
>The 'employment' section describes the candidate's formal education, including college and university, continuing education, and standalone programs and courses.

In addition to history and summary this also has `level`, one's highest-level of education, and `dergee`, the type of one's highest degree.

field | description
--- | --- | ---
title | A freeform title for this education stint. Typically, this should be the short name of your degree, certification, or training.
institution | College or school name.
area | e.g. Arts
studyType | e.g. Bachelor
start | Date this schooling began, in YYYY, YYYY-MM, or YYYY-MM-DD format.
end | Date this schooling ended, in YYYY, YYYY-MM, or YYYY-MM-DD format.
grade | Grade or GPA.
curriculum | Notable courses, subjects, and educational experiences.
url | Website or URL of the institution or school.
summary | A short summary of this education experience.
keywords | Keywords associated with this education stint.
highlights | Noteworthy achievements and/or highlights.
location | Freeform location of the education, e.g., 'San Francisco, CA' or 'Tokyo'.


### affiliation
> membership in groups, clubs, organizations, and professional associations whether at the collegiate, corporate, or personal level.

field | description
--- | --- | ---
category | The type of affiliation: club, union, meetup, etc.
organization | The name of the organization or group.
role | Your role in the organization or group.
url | Organization website.
start | Date your affiliation with the organization began, in YYYY, YYYY-MM, or YYYY-MM-DD format.
end | Date your affiliation with the organization ended, in YYYY, YYYY-MM, or YYYY-MM-DD format.
summary | A summary of your achievements and responsibilities during this affiliation.
highlights | Noteworthy achievements and/or highlights.
keywords | Keywords associated with this affiliation.
location | Freeform location of the position, e.g., 'San Francisco, CA' or 'Tokyo'.


## Lists
These are simple arrays of items.  Each defines different fields for its units, shown below.

### projects
> project history -- not the jobs the candidate has worked but the specific projects and enterprises the candidate has created or been involved in, whether paid or unpaid.

field | description
--- | --- | ---
title | Project name or code-name.
category | Project type: open-source, private, side project, etc.
description | Project description or summary.
summary | A summary of your achievements and responsibilities on the project.
role | Your role on the project: Contributor, Creator, etc.
url | Project URL.
media | Media associated with this project.
repo | Repo URL.
start | Date your involvement with project began, in YYYY, YYYY-MM, or YYYY-MM-DD format.
end | Date your involvement with project ended, in YYYY, YYYY-MM, or YYYY-MM-DD format.
highlights | Noteworthy project-related achievements and/or highlights.
location | Freeform location of the job or position, e.g., 'San Francisco, CA' or 'Tokyo'.
keywords | Keywords associated with this project.


### social
> participation in internet and social networking services and communities including GitHub, FaceBook, and the like.

field | description
--- | --- | ---
network | The name of the social network, such as Facebook or GitHub.
user | Your username or handle on the social network.
url | URL of your profile page on this network.
label | A friendly label.


### recognition
> public or professional plaudits, kudos, awards, and other forms of positive external reinforcement.

field | description
--- | --- | ---
category | Type of recognition: award, honor, prize, etc.
title | Title of the award or recognition.
date | Date awarded, in YYYY, YYYY-MM, or YYYY-MM-DD format.
from | Name of the awarding company, insitution, or individual.
summary | A brief description of the award and why you received it.
url | A webpage or other associated URL.



### writing
> writing and publication history, from blogs and essays to novels and dissertations.

field | description
--- | --- | ---
title | Title of the article, essay, or book.
category | One of 'book', 'article', 'essay', 'blog post', or 'series'.
publisher | Publisher of the article, essay, or book.
date | Publication date in YYYY, YYYY-MM, or YYYY-MM-DD format.
url | Website or URL of this writing or publication.
summary | A brief summary of the publication.


### reading
> reading habits and is intended to demonstrate familiarity with industry-relevant publications, blogs, books, or other media that a competent industry candidate should be expected to know.

field | description
--- | --- | ---
title | Title of the book, blog, or article.
category | The type of reading: book, article, blog, magazine, series, etc.
url | URL of the book, blog, or article.
author | Author of the book, blog, or article.
date | Publication date in YYYY, YYYY-MM, or YYYY-MM-DD format.
summary | A brief description of the book, magazine, etc.



### governance
> leadership, standards, board, and committee roles.

field | description
--- | --- | ---
summary | Summary of your governance at this organization.
category | Type of governance: committee, board, standards group, etc.
role | Governance role: board member, contributor, director, etc.
organization | The organization.
start | Start date.
end | End date.
keywords | Keywords associated with this governance stint.
highlights | Noteworthy achievements and/or highlights.



### languages
> knowledge of world languages such as English, Spanish, or Chinese.

field | description
--- | --- | ---
language | The name of the language: English, Spanish, etc.
level | Level of fluency with the language, from 1 to 10.
years | Amount of time language spoken?

### samples
>The 'samples' section provides an accessible demonstration of the candidate's portfolio or work product to potential employers and co-workers.

field | description
--- | --- | ---
title | Title or descriptive name.
summary | A brief description of the sample.
url | URL of the sample (if any).
date | Date the sample was released in YYYY, YYYY-MM, or YYYY-MM-DD format.
highlights | Noteworthy achievements and/or highlights for this sample.
keywords | Keywords associated with this work sample.


### references
> personal, professional, and/or technical references.

field | description
--- | --- | ---
name | The full name of the person giving the reference.
role | The occupation of this reference, or his or her relationship to the candidate.
category | The type of reference, eg, professional, technical, or personal.
private | Is this a private reference?
summary | Optional summary information for this reference.
contact | List of contact methods for this reference.


### testimonials
>The 'testimonials' section contains public testimonials of the candidate's professionalism and character.

field | description
--- | --- | ---
name | The full name of the person giving the reference.
quote | A quoted reference, eg, 'Susan was an excellent team leader, manager, and operations specialist with a great eye for detail. I'd gladly hire her again if I could!'
category | Type of reference: personal, professional, or technical.
private | Public reference (testimonial) or via private contact?


### interests
>The 'interests' section provides a sampling of the candidate's interests and enthusiasms outside of work.

field | description
--- | --- | ---
name | The name or title of the interest or hobby.
summary |
keywords | list of associated keywords

### extracurricular
> involvement with industry-related events and enterprises outside of work. For example: attending conferences, workshops, or meetups.

field | description
--- | --- | ---
title | Title of the extracurricular activity.
activity | The extracurricular activity.
location | City, state, or other freeform location.
start | Start date.
end | End date.


## Other


### skills
>A description of the candidate's formal skills and capabilities.

This is formatted a little differently.  It contains `sets` and `list`.  The elements of `sets` must reference one or more skills described in `list`

#### list
List of skills with the following fields

field | description
--- | --- | ---
name | The name or title of the skill.
level | A freeform description of your level of mastery with the skill.
summary | A short summary of your experience with this skill.
years | Number of years you've used the skill.


#### sets
List of skillsets grouping together skills from `list`

field | description
--- | --- | ---
name | Name of the skillset: 'Programming' or 'Project Management' etc.
level | Level of mastery of the skill.
skills | "Title or ID of a skill from the skills list."
