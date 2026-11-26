# PRODUCT REQUIREMENTS DOCUMENT

## Campus Lost-and-Found Management System

| Document detail | Information |
|---|---|
| Course | BU-209 innovation in web designa and development |
| Assignment | Week 4 – Product Requirements Document |
| Team name | **CodeX** |
| Project | Campus Lost-and-Found Management System |
| Version | 1.1 |
| Date | 25 November 2026 |
| Document status | Revised team draft – confirm open decisions before submission |

---

## 1. Introduction

Students move between lecture halls, laboratories, libraries, hostels and other campus facilities. During these activities, personal belongings such as books, phones, keys, identity cards, wallets and water bottles can be misplaced. When an item is found, the person who finds it may not know how to reach its owner. A student who has lost something may also be unsure where to ask or whether the item has already been found.

The Campus Lost-and-Found Management System is a proposed web application that provides a central place for reporting and searching for found belongings. For the first version (the Minimum Viable Product, or MVP), users will be able to report found items, view reports, search and filter the reports, and update an item's status after it has been returned.

**MVP scope clarification:** This first version accepts reports of *found items only*. A student who has lost an item can search the existing found-item reports, but cannot create a separate lost-item report in the MVP. A lost-item reporting feature may be considered for a later version.

## 2. Problem statement

Students may experience difficulty recovering belongings misplaced within the campus environment. Information about found property may be shared through informal channels such as class group chats, course representatives, friends, departmental offices or security points. When information is spread across different channels, a student may not know which source to check. Messages can also become difficult to find in busy group conversations.

The proposed system will bring found-item reports together in one searchable location. It is intended to support existing campus procedures rather than replace the staff or security personnel responsible for keeping valuable items safe.

## 3. Problem context and initial analysis

The project is designed to address these situations:

1. A student misplaces an item and needs a convenient way to check whether it has been found.
2. A student or staff member finds an item and needs a consistent way to share information about it.
3. A person responsible for keeping a found item needs to communicate its collection location and update its status after it is returned.

### 3.1 People affected

- **Students who lose items:** need to search reports and find out where to ask about a possible match.
- **Students or staff who find items:** need to report what they found without exposing sensitive information.
- **Campus office or security personnel:** may receive found property and help verify ownership and arrange collection.

### 3.2 Existing ways of handling lost property

Possible methods include asking friends or classmates, posting in class or departmental messaging groups, contacting a course representative, revisiting the location where the item was last seen, or asking at a departmental office or security point. These methods are familiar, but information may be distributed across several places.

### 3.3 Gaps the proposed system addresses

- There may be no single searchable list of reported found items.
- A message about a found item may be overlooked in a busy group chat.
- Students may not know which office or person to contact.
- It may be difficult to know whether an item is still available or has already been collected.

These points are the team's initial problem analysis and should be treated as assumptions until confirmed through feedback from students and the relevant campus office. The team has not claimed to have completed a formal survey or confirmed an official campus procedure unless it has actually done so.

## 4. Project aim and objectives

### 4.1 Aim

To develop a simple web-based platform that helps members of the campus community report, search for and track found belongings.

### 4.2 Objectives

- Provide a central list of found-item reports.
- Allow a finder to submit the details of an item.
- Allow students to search reports by item name, location, description or collection point.
- Allow users to filter reports by category and status.
- Display where an item was found and where the owner can ask about collection.
- Allow a report's status to be updated after the item has been returned.
- Keep the first version small enough to test with a limited student group.

## 5. Proposed solution

The proposed solution is a browser-based Lost-and-Found Board. A person who finds an item opens the application and submits a report containing the item's general name, category, location, date found, short description and collection point. The report is saved and displayed on the board.

A student who has lost an item can open the board, search using a keyword and filter the reports by category or status. If a report appears to match the lost item, the student can visit the stated collection point and follow the collection process. The person holding the item should verify ownership before handing it over. Once collection has been confirmed, the report can be marked as returned.

The public report should not reveal every identifying detail of the item. This helps the person holding the item ask the claimant to provide information that can be used to verify ownership.

## 6. Target users and user stories

### 6.1 Target users

| User | Need |
|---|---|
| Student who lost an item | Search reports and find out where to ask about a possible match. |
| Person who found an item | Record the item and provide useful collection information. |
| Campus staff or security contact | Help manage collection and confirm when an item has been returned. |

### 6.2 User stories

- As a student who has lost an item, I want to search found-item reports so that I can check whether someone has found it.
- As a person who finds an item, I want to submit a report so that its owner can locate it.
- As a user, I want to filter reports by category so that I can find relevant items more quickly.
- As a user, I want to filter reports by status so that I can focus on items that may still be available.
- As the person authorised to update a report, I want to mark an item as returned so that users can see its current status.

## 7. Minimum viable product (MVP)

The MVP will contain the functions needed to demonstrate the main found-item reporting and retrieval process.

| ID | Feature | Priority | Acceptance criteria |
|---|---|---|---|
| FR-01 | Add found item | Must have | When all required fields contain valid information, the system saves the report, assigns it a unique ID and displays it on the board. |
| FR-02 | View reports | Must have | Users can view saved reports with the key item details and status. |
| FR-03 | Search | Must have | Search returns reports matching the entered text in the item name, location, description or collection point. Search is case-insensitive and supports partial words. |
| FR-04 | Category filter | Should have | Selecting a category displays only reports in that category. |
| FR-05 | Status filter | Should have | Users can choose to view Available reports or all reports. |
| FR-06 | Collection details | Must have | Each report displays the general location where it was found and the collection point. |
| FR-07 | Mark as returned | Should have | An authorised prototype action changes an item's status from Available to Returned and records the return date. |
| FR-08 | Input validation | Must have | Required fields, date values and categories are validated before a report is saved. |
| FR-09 | Empty and error messages | Must have | The system displays a helpful message when there are no reports, no search matches, or a request fails. |

### 7.1 Categories

The MVP should use a consistent set of categories. The team may adjust these before implementation to suit the campus:

- Electronics (phones, chargers, earphones)
- Identification (student ID cards and other identity cards)
- Books and stationery
- Bags
- Clothing
- Keys
- Accessories
- Other

### 7.2 Status definitions

| Status | Meaning |
|---|---|
| Available | The item has been found and is believed to be awaiting collection. |
| Returned | Collection has been confirmed and the item has been handed back to its owner. |

### 7.3 Features outside the MVP

The first version will not include separate lost-item submissions, a mobile application, online payments, delivery services, facial recognition, automatic owner identification, live chat, push notifications, image uploads, campus-wide single sign-on or full user-account management. These features may be considered in a later version if feedback and project resources justify them.

For the class prototype, the team may demonstrate the returned-status action without login. In a real deployment, the action must be restricted to an authorised person, such as a designated campus staff member or the person managing the item. The exact permission model is an open decision to confirm before deployment.

## 8. Functional requirements

1. The system shall allow a user to submit a found-item report.
2. The system shall require an item name, category, found location, date found, description and collection point.
3. The system shall assign a unique identifier to each report.
4. The system shall save reports so they remain available after a page refresh.
5. The system shall display saved reports in a list or card layout.
6. The system shall support keyword search across the item name, location, description and collection point.
7. Search shall be case-insensitive and shall support partial-word matches.
8. The system shall allow filtering by category and status.
9. The system shall display a clear message when no report matches a search or filter.
10. The system shall display a helpful message if there are no reports yet.
11. The system shall allow an authorised prototype action to mark a report as returned.
12. The system shall reject invalid or incomplete submissions and display an understandable error message.
13. The found date shall be valid and shall not be later than the current date.
14. The system shall display an understandable error if reports cannot be retrieved or saved because of a server or storage problem.
15. The system shall not display sensitive personal details in public item reports.

## 9. Non-functional requirements

- **Usability:** Forms and search controls should be simple enough for a first-time user to understand.
- **Responsiveness:** The interface should work on common mobile and desktop screen sizes.
- **Performance:** The small pilot list should load without unnecessary delay on a normal internet connection.
- **Reliability:** Saved reports should remain available after the page is refreshed and after a normal server restart, subject to the chosen storage method.
- **Privacy:** Public reports must not contain phone numbers, student identification numbers, home addresses or other private details. Descriptions should avoid revealing every identifying detail of an item.
- **Security:** The backend must validate incoming data. In a real deployment, actions such as moderation and marking an item as returned must be restricted to authorised users.
- **Maintainability:** The code should be separated into clear frontend, backend and data-storage responsibilities.
- **Error handling:** The application should communicate failures in a way users can understand and should not expose sensitive technical details.

## 10. System workflow

### 10.1 Finder workflow

1. The finder opens the Lost-and-Found Board.
2. The finder selects the form for reporting a found item.
3. The finder enters the item's general details and collection point.
4. The system validates the submitted information.
5. If the information is valid, the system saves the report and displays it on the board.
6. If the information is invalid or saving fails, the system displays an error and allows the finder to correct or retry.

### 10.2 Owner workflow

1. The student opens the board.
2. The student enters a keyword or selects a category/status filter.
3. The system displays matching reports.
4. The student checks the general description and collection point.
5. The student visits the stated collection point and follows the collection procedure.
6. The person holding the item verifies ownership before handover, using identifying information that is not fully disclosed in the public report.
7. After collection is confirmed, an authorised person marks the report as Returned.

## 11. Data requirements

Each found-item record will contain the following fields:

| Field | Data type | Required? | Description |
|---|---|---|---|
| id | String | System-generated | Unique identifier for the report. |
| name | String | Yes | General name of the item. |
| category | String | Yes | Category selected from the approved options. |
| location | String | Yes | General campus location where the item was found. |
| foundDate | Date | Yes | Date the item was found; must not be in the future. |
| description | String | Yes | Short public description that does not reveal every identifying detail. |
| collectionPoint | String | Yes | Office or approved location where the owner can ask about collection. |
| status | String | System-generated/default | Available or Returned. A new report defaults to Available. |
| createdAt | Date/time | System-generated | Date and time the report was created. |
| returnedAt | Date/time | Conditional | Date and time the item was marked as returned; empty/null while Available. |

The backend should trim input values and reject required fields that are empty or contain only spaces. It should also reject unsupported categories and invalid dates.

Duplicate reports may occur if more than one person reports the same item. Automatic duplicate detection is outside the MVP; duplicates may be reviewed manually during the prototype.

## 12. Backend/API requirements

The prototype is expected to provide the following API endpoints. The exact implementation should be checked against the team's existing backend code before this section is finalised.

| HTTP method | Endpoint | Purpose |
|---|---|---|
| GET | `/api/items` | Retrieve found-item reports. May accept optional search, category and status query parameters. |
| POST | `/api/items` | Validate and create a found-item report. |
| PATCH | `/api/items/:id/returned` | Mark a report as returned and record the return date, subject to the prototype's permission approach. |

### 12.1 GET endpoint query examples

These are examples of possible query parameters, not confirmation that they have already been implemented:

- `/api/items` — retrieve reports.
- `/api/items?search=phone` — search for a keyword.
- `/api/items?category=Electronics` — filter by category.
- `/api/items?status=Available` — filter by status.

If the frontend performs filtering after retrieving the reports, the team should document that approach instead. The PRD and code should describe the same behavior.

### 12.2 API behavior

- The backend shall validate submitted data before saving it.
- The backend shall generate unique IDs rather than relying on users to provide them.
- The backend shall return JSON responses.
- Requests for an item that does not exist shall return an appropriate error.
- Invalid submissions shall return an error response with a message the frontend can display.
- Server or storage failures shall be handled without exposing sensitive internal details.
- In a deployed version, the returned-status endpoint shall require appropriate authorization.

## 13. Proposed technology and implementation approach

The team intends to use web technologies for the prototype. The exact storage and package details must be confirmed against the current repository so that this PRD remains accurate.

| Technology | Intended role |
|---|---|
| HTML | Structure of the web pages and forms. |
| CSS | Layout, colours and responsive styling. |
| JavaScript | Browser interactions, API communication, search and filtering. |
| Node.js | Backend server and API endpoints. |
| Storage | **Confirm against the current project code** (for example, JSON-file storage or a database). |

A simple storage method may be acceptable for a classroom prototype with a small amount of data. If the application is intended for multiple users or real campus use, the team should use a suitable database and plan for backups, access control and concurrent updates.

**Verification note before submission:** Confirm whether the actual project uses a JSON file, database, Express or other npm packages, and update this section to match. Do not claim that no third-party packages are used unless the repository confirms it.

## 14. Validation and testing plan

The following tests will be used to check the MVP:

| Test | Action | Expected result |
|---|---|---|
| T01 | Submit a report with all required fields and valid values | The report is saved, assigned an ID and displayed. |
| T02 | Submit a report with a required field missing | The system rejects it and shows an error. |
| T03 | Submit a required field containing only spaces | The system rejects it and asks for a valid value. |
| T04 | Submit an invalid or future found date | The system rejects it and displays a date-validation message. |
| T05 | Search using part of an item name | Matching reports are displayed. |
| T06 | Search using different letter casing | The same relevant results are returned. |
| T07 | Search using a campus location | Reports matching the location are displayed. |
| T08 | Select a category filter | Only reports in that category are displayed. |
| T09 | Select Available status | Returned reports are excluded. |
| T10 | Refresh the browser | Previously saved reports remain visible. |
| T11 | Mark an available report as returned | Its status changes to Returned and the return date is recorded. |
| T12 | Search for a word with no match | A no-results message is displayed. |
| T13 | Open the board when there are no saved reports | An empty-state message is displayed. |
| T14 | Simulate or encounter a server/storage failure | A helpful error message is displayed. |
| T15 | Open the page on a mobile-sized screen | The layout remains readable and usable. |

## 15. Risks and mitigation

| Risk | Effect | Mitigation |
|---|---|---|
| False reports | Users may be misdirected. | Consider report review or moderation for a real deployment. |
| False ownership claims | An item could be handed to the wrong person. | Keep an identifying detail private and verify ownership at collection. |
| Personal information exposed | A student's privacy may be affected. | Do not request or publish sensitive personal details. |
| Old reports remain visible | Users may search for items already collected. | Update the status promptly after handover. |
| Low adoption | Few students may use the platform. | Pilot with a defined student group and gather feedback. |
| Loss of prototype data | Reports could be lost if local files are deleted or damaged. | Keep a backup during the prototype; use managed storage and backups for a real service. |
| Unauthorized status changes | An item may be incorrectly shown as returned. | Restrict this action in a real deployment; document the prototype's demonstration permissions. |
| Duplicate reports | Multiple entries may describe the same item. | Review duplicates manually during the MVP. |

## 16. Success measures

The pilot can be evaluated using the following measures:

- Number of found-item reports submitted.
- Number and proportion of reports marked as returned.
- Time taken by a test user to locate a matching report.
- Whether users can complete the reporting form without assistance.
- Feedback from students and the campus contact responsible for found property.
- Common problems or suggestions reported during testing.

The team should record actual results during testing rather than assume that the system has achieved these outcomes. If the team sets numeric targets, those targets should be agreed before the pilot and clearly identified as goals rather than results.

## 17. Limitations and future improvements

The initial prototype is intended to demonstrate the main workflow. It does not yet provide separate lost-item submissions, full user accounts, staff roles, report approval, image uploads, notifications, audit logs, production-level access control or production-grade backups. The storage method may also limit concurrent use, depending on the implementation.

Possible future improvements include user authentication, staff moderation, image attachments, email notifications, automatic expiry of old reports, a database, usage analytics and deployment on an approved campus server. These improvements should be prioritised based on feedback from the pilot.

## 18. Conclusion

The Campus Lost-and-Found Management System aims to make it easier for students to report and search for belongings found around campus. By bringing reports into one searchable board and displaying a collection point and status for each item, the proposed MVP addresses some of the communication and tracking steps involved in returning found property.

The first version will remain focused on reporting found items, viewing, searching, filtering and updating item status. A small pilot and feedback from students and the relevant campus office will help the team decide what should be improved before the system is expanded.

---

**Prepared by:** Team CodeX  
**Course:** BU-209 Backend Engineering  
**Deliverable:** Week 4 – PRD.md

---

