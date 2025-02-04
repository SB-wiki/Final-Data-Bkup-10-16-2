---
icon: elementor
---

# Modifications-to-download-Course-Progress-Report

IntroductionStates will be rolling out their training programs. One key aspect is to help them provide targetted information so that they can monitor the progress of their teachers. In this context, the following fields are to be added to the download report:

a) External ID

b) User ID

c) Block name

d) Course completion date

User StoryAs a course mentor, when I download the report, I want to be able to see the block information so that I can filter the report by block and share it with the respective block nodal officer.

As a course mentor, when I download the report, I want to be able to see the teacher's state unique ID so that I can identify the teacher and reward those who have completed the course.

As a course mentor for a state with no unique ID, when I download the report, I want to be able to see the teacher's DIKSHA user id so that I use this to uniquely identify the teacher and reward those who have completed the course.

As a course mentor, when I download the report, I want to be able to see the teacher's course completion date.

ScopeThe scope is to include three new fields in the download extract:

**External ID** - This is the unique ID which the state provides to the teachers and the teachers use this ID to login to Diksha from the State portal. In the case of AP it would be teachers' APEKX id. If the ID is not available then leave the field blank.

\*\*User id - \*\* This is the DIKSHA user ID which is generated by DIKSHA and is made available to the user on their profile page. This ID cannot be blank.

\*\*Block - \*\* This is the user’s block information to be added from user profile data. If the ID is not available for the user leave it blank.

**Completion Date** - this is the date when the user completed the course.

The sequence of the fields of this CSV are to be in the following format:

a) External ID

b) User ID

b) User Name

c) Email ID

d) Mobile Number

e) Organization Name

f) District Name

g) School Name

h) Block Name

h) Enrollment Date

i) Course Progress

j) Completion Date

[SB-13080 System JIRA](https://browse/SB-13080)ExceptionsIf any of these fields do not have a value leave it as blank in the csv file.

Localization RequirementsUse this section to provide requirements to localize static content and/or design elements that are part of the UI in the following table. Localization of either the framework, content or search elements should be elaborated as a user story. To add or remove rows in the table, use the table functionality from the toolbar.  &#x20;

| UI Element | Description | Language(s)/ Locales Required |
| ---------- | ----------- | ----------------------------- |
| None       |             |                               |

Telemetry Requirements

| Event Name                                         | Description                                                                                       | Purpose                                                                                                     |
| -------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| Click 'Download File' in the course dashboard page | Mentor can download the report by clicking on 'Download File' button in the course dashboard page | This data will tell us how many users are actually clicking on this button to download the progress report. |

Non-Functional RequirementsUse this section to capture non-functional requirements in the following table. To add or remove rows in the table, use the table functionality from the toolbar.  &#x20;

| Performance / Responsiveness Requirements                                                                                                                                                                                                      | Load/Volume Requirements | Security / Privacy Requirements |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------ | ------------------------------- |
| <ul><li>Download file to support batch size upto upto 1L</li><li>Downloaded file is sent as an email attachment to the requestors email ID. The time lapsed between the request and receipt of the email should not exceed 30 mins. </li></ul> |                          |                                 |
|                                                                                                                                                                                                                                                |                          |                                 |

Impact on other Products/SolutionsUse this section to capture the impact of this use case on other products, solutions. To add or remove rows in the table, use the table functionality from the toolbar.  &#x20;

| Product/Solution Impacted | Impact Description |
| ------------------------- | ------------------ |
| None                      |                    |

Impact on Existing Users/Data Use this section to capture the impact of this use case on existing users or data. To add or remove rows in the table, use the table functionality from the toolbar.  &#x20;

| User/Data Impacted | Impact Description |
| ------------------ | ------------------ |
| None               |                    |
|                    |                    |

Key MetricsSpecify the key metrics that should be tracked to measure the effectiveness of this use case in the following table. To add or remove rows, use the table functionality from the toolbar

| Srl. No. | Metric                                                                                                                                                                                                                                   | Purpose of Metric                                                                                                                 |
| -------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| 1        | <p><strong>download ratio per batch</strong>  = no. of times the file was downloaded/no. of batchesThis ratio to be monitored at the level of:</p><ul><li>individual course and</li><li>all courses </li><li>individual tenant</li></ul> | This metric will provide insights on whether state admins are downloading the report to track the course completion of the users. |

***

\[\[category.storage-team]] \[\[category.confluence]]
