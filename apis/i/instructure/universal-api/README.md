# <img src="https://images.mindcloud.co/apps/icons/instructure-canvas-icon_1775484647287.png" alt="Instructure logo" width="28" height="28"> Instructure: Universal API

Canvas LMS by Instructure. Access users, courses, assignments, modules, pages, files, enrollments, calendar events, announcements, and discussion topics through the Canvas REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/instructure/latest
- **Actions:** 115
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.instructure.com/canvas
- **Vendor API docs:** https://developerdocs.instructure.com/services/canvas

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (115)

### Activity Stream Item

| Action | Method | Description |
| --- | --- | --- |
| [Hide All Stream Items](actions/hide-all-stream-items.md) | DELETE | Hides all stream items in Instructure Canvas. |
| [List Activity Stream](actions/list-activity-stream.md) | GET | Retrieves the activity stream from Instructure Canvas. |

### Activity Stream Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Activity Stream Summary](actions/get-activity-stream-summary.md) | GET | Retrieves the activity stream summary from Instructure Canvas. |

### Announcement

| Action | Method | Description |
| --- | --- | --- |
| [List Announcements](actions/list-announcements.md) | GET | Retrieves announcements from Instructure Canvas. |

### Assignment

| Action | Method | Description |
| --- | --- | --- |
| [Create Assignment](actions/create-assignment.md) | POST | Creates a new assignment in Instructure Canvas. |
| [Delete Assignment](actions/delete-assignment.md) | DELETE | Deletes an assignment from Instructure Canvas. |
| [Get Assignment](actions/get-assignment.md) | GET | Retrieves an assignment from Instructure Canvas. |
| [List Assignments](actions/list-assignments.md) | GET | Retrieves assignments from Instructure Canvas. |
| [Update Assignment](actions/update-assignment.md) | PUT | Updates an existing assignment in Instructure Canvas. |

### Bookmark

| Action | Method | Description |
| --- | --- | --- |
| [Create Bookmark](actions/create-bookmark.md) | POST | Creates a new bookmark in Instructure Canvas. |
| [Delete Bookmark](actions/delete-bookmark.md) | DELETE | Deletes a bookmark from Instructure Canvas. |
| [Get Bookmark](actions/get-bookmark.md) | GET | Retrieves a bookmark from Instructure Canvas. |
| [List Bookmarks](actions/list-bookmarks.md) | GET | Retrieves bookmarks from Instructure Canvas. |
| [Update Bookmark](actions/update-bookmark.md) | PUT | Updates an existing bookmark in Instructure Canvas. |

### Calendar Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Calendar Event](actions/create-calendar-event.md) | POST | Creates a new calendar event in Instructure Canvas. |
| [Delete Calendar Event](actions/delete-calendar-event.md) | DELETE | Deletes a calendar event from Instructure Canvas. |
| [Get Calendar Event](actions/get-calendar-event.md) | GET | Retrieves a calendar event from Instructure Canvas. |
| [List Calendar Events](actions/list-calendar-events.md) | GET | Retrieves calendar events from Instructure Canvas. |
| [Update Calendar Event](actions/update-calendar-event.md) | PUT | Updates an existing calendar event in Instructure Canvas. |

### Communication Channel

| Action | Method | Description |
| --- | --- | --- |
| [List Communication Channels](actions/list-communication-channels.md) | GET | Retrieves communication channels from Instructure Canvas. |

### Content Share

| Action | Method | Description |
| --- | --- | --- |
| [List Received Content Shares](actions/list-received-content-shares.md) | GET | Retrieves received content shares from Instructure Canvas. |
| [List Sent Content Shares](actions/list-sent-content-shares.md) | GET | Retrieves sent content shares from Instructure Canvas. |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves conversations from Instructure Canvas. |
| [Mark All Conversations As Read](actions/mark-all-conversations-as-read.md) | PUT | Marks all conversations as read in Instructure Canvas. |

### Conversation Batch

| Action | Method | Description |
| --- | --- | --- |
| [Get Conversation Batches](actions/get-conversation-batches.md) | GET | Retrieves conversation batches from Instructure Canvas. |

### Course

| Action | Method | Description |
| --- | --- | --- |
| [Get Course](actions/get-course.md) | GET | Retrieves a course from Instructure Canvas. |
| [List Courses](actions/list-courses.md) | GET | Retrieves courses from Instructure Canvas. |

### Course Nickname

| Action | Method | Description |
| --- | --- | --- |
| [Clear Course Nicknames](actions/clear-course-nicknames.md) | DELETE | Clears course nicknames from Instructure Canvas. |
| [List Course Nicknames](actions/list-course-nicknames.md) | GET | Retrieves course nicknames from Instructure Canvas. |

### Dashboard Position

| Action | Method | Description |
| --- | --- | --- |
| [Get Dashboard Positions](actions/get-dashboard-positions.md) | GET | Retrieves dashboard positions from Instructure Canvas. |

### Discussion Topic

| Action | Method | Description |
| --- | --- | --- |
| [Create Discussion Topic](actions/create-discussion-topic.md) | POST | Creates a new discussion topic in Instructure Canvas. |
| [Delete Discussion Topic](actions/delete-discussion-topic.md) | DELETE | Deletes a discussion topic from Instructure Canvas. |
| [Get Discussion Topic](actions/get-discussion-topic.md) | GET | Retrieves a discussion topic from Instructure Canvas. |
| [List Discussion Topics](actions/list-discussion-topics.md) | GET | Retrieves discussion topics from Instructure Canvas. |
| [Update Discussion Topic](actions/update-discussion-topic.md) | PUT | Updates an existing discussion topic in Instructure Canvas. |

### Enrollment

| Action | Method | Description |
| --- | --- | --- |
| [Get Enrollment](actions/get-enrollment.md) | GET | Retrieves an enrollment from Instructure Canvas. |
| [List Course Enrollments](actions/list-course-enrollments.md) | GET | Retrieves course enrollments from Instructure Canvas. |

### Favorite

| Action | Method | Description |
| --- | --- | --- |
| [Add Course To Favorites](actions/add-course-to-favorites.md) | POST | Adds a course to favorites in Instructure Canvas. |
| [Add Group To Favorites](actions/add-group-to-favorites.md) | POST | Adds a group to favorites in Instructure Canvas. |
| [Remove Course From Favorites](actions/remove-course-from-favorites.md) | DELETE | Removes a course from favorites in Instructure Canvas. |
| [Remove Group From Favorites](actions/remove-group-from-favorites.md) | DELETE | Removes a group from favorites in Instructure Canvas. |
| [Reset Course Favorites](actions/reset-course-favorites.md) | DELETE | Resets course favorites in Instructure Canvas. |
| [Reset Group Favorites](actions/reset-group-favorites.md) | DELETE | Resets group favorites in Instructure Canvas. |

### Favorite Course

| Action | Method | Description |
| --- | --- | --- |
| [List Favorite Courses](actions/list-favorite-courses.md) | GET | Retrieves favorite courses from Instructure Canvas. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Get File](actions/get-file.md) | GET | Retrieves a file from Instructure Canvas. |
| [List Folder Files](actions/list-folder-files.md) | GET | Retrieves files in a folder from Instructure Canvas. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | DELETE | Deletes a file from Instructure Canvas. |
| [List User Files](actions/list-user-files.md) | GET | Retrieves user files from Instructure Canvas. |
| [Update File](actions/update-file.md) | PUT | Updates a file in Instructure Canvas. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new folder in Instructure Canvas. |
| [Delete Folder](actions/delete-folder.md) | DELETE | Deletes a folder from Instructure Canvas. |
| [Get Folder](actions/get-folder.md) | GET | Retrieves a folder from Instructure Canvas. |
| [List User Folders](actions/list-user-folders.md) | GET | Retrieves user folders from Instructure Canvas. |
| [Update Folder](actions/update-folder.md) | PUT | Updates an existing folder in Instructure Canvas. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [List Favorite Groups](actions/list-favorite-groups.md) | GET | Retrieves favorite groups from Instructure Canvas. |
| [List User Groups](actions/list-user-groups.md) | GET | Retrieves user groups from Instructure Canvas. |

### Missing Submission

| Action | Method | Description |
| --- | --- | --- |
| [List Missing Submissions](actions/list-missing-submissions.md) | GET | Retrieves missing submissions from Instructure Canvas. |

### Module

| Action | Method | Description |
| --- | --- | --- |
| [Get Module](actions/get-module.md) | GET | Retrieves a module from Instructure Canvas. |
| [List Modules](actions/list-modules.md) | GET | Retrieves modules from Instructure Canvas. |

### Module Item

| Action | Method | Description |
| --- | --- | --- |
| [List Module Items](actions/list-module-items.md) | GET | Retrieves module items from Instructure Canvas. |

### Notification Preference

| Action | Method | Description |
| --- | --- | --- |
| [Get Notification Preference](actions/get-notification-preference.md) | GET | Retrieves a notification preference from Instructure Canvas. |
| [List Notification Preferences](actions/list-notification-preferences.md) | GET | Retrieves notification preferences from Instructure Canvas. |
| [Update Multiple Notification Preferences](actions/update-multiple-notification-preferences.md) | PUT | Updates multiple notification preferences in Instructure Canvas. |
| [Update Notification Preference](actions/update-notification-preference.md) | PUT | Updates a notification preference in Instructure Canvas. |

### Notification Preference Category

| Action | Method | Description |
| --- | --- | --- |
| [List Notification Preference Categories](actions/list-notification-preference-categories.md) | GET | Retrieves notification preference categories from Instructure Canvas. |
| [Update Notification Preferences By Category](actions/update-notification-preferences-by-category.md) | PUT | Updates notification preferences by category in Instructure Canvas. |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Create Page](actions/create-page.md) | POST | Creates a new page in Instructure Canvas. |
| [Delete Page](actions/delete-page.md) | DELETE | Deletes a page from Instructure Canvas. |
| [Get Page](actions/get-page.md) | GET | Retrieves a page from Instructure Canvas. |
| [List Pages](actions/list-pages.md) | GET | Retrieves pages from Instructure Canvas. |
| [Update Page](actions/update-page.md) | PUT | Updates an existing page in Instructure Canvas. |

### Page View

| Action | Method | Description |
| --- | --- | --- |
| [List Page Views](actions/list-page-views.md) | GET | Retrieves page views from Instructure Canvas. |

### Planner Item

| Action | Method | Description |
| --- | --- | --- |
| [List Planner Items](actions/list-planner-items.md) | GET | Retrieves planner items from Instructure Canvas. |

### Planner Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Planner Note](actions/create-planner-note.md) | POST | Creates a new planner note in Instructure Canvas. |
| [Delete Planner Note](actions/delete-planner-note.md) | DELETE | Deletes a planner note from Instructure Canvas. |
| [Get Planner Note](actions/get-planner-note.md) | GET | Retrieves a planner note from Instructure Canvas. |
| [List Planner Notes](actions/list-planner-notes.md) | GET | Retrieves planner notes from Instructure Canvas. |
| [Update Planner Note](actions/update-planner-note.md) | PUT | Updates an existing planner note in Instructure Canvas. |

### Planner Override

| Action | Method | Description |
| --- | --- | --- |
| [Create Planner Override](actions/create-planner-override.md) | POST | Creates a new planner override in Instructure Canvas. |
| [Delete Planner Override](actions/delete-planner-override.md) | DELETE | Deletes a planner override from Instructure Canvas. |
| [Get Planner Override](actions/get-planner-override.md) | GET | Retrieves a planner override from Instructure Canvas. |
| [List Planner Overrides](actions/list-planner-overrides.md) | GET | Retrieves planner overrides from Instructure Canvas. |
| [Update Planner Override](actions/update-planner-override.md) | PUT | Updates an existing planner override in Instructure Canvas. |

### Todo Item

| Action | Method | Description |
| --- | --- | --- |
| [List Todo Items](actions/list-todo-items.md) | GET | Retrieves todo items from Instructure Canvas. |

### Todo Item Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Todo Item Count](actions/get-todo-item-count.md) | GET | Retrieves the todo item count from Instructure Canvas. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Course Section](actions/create-course-section.md) | POST | Creates a new course section in Instructure Canvas. |
| [Delete Section](actions/delete-section.md) | DELETE | Deletes a section from Instructure Canvas. |
| [Get Course Nickname](actions/get-course-nickname.md) | GET | Retrieves a course nickname from Instructure Canvas. |
| [Get Custom Color](actions/get-custom-color.md) | GET | Retrieves a custom color from Instructure Canvas. |
| [Get File Public Preview URL](actions/get-file-public-preview-url.md) | GET | Retrieves a file public preview URL from Instructure Canvas. |
| [Get Graded Submissions](actions/get-graded-submissions.md) | GET | Retrieves graded submissions from Instructure Canvas. |
| [Get Page Views Query Status](actions/get-page-views-query-status.md) | GET | Retrieves page views query status from Instructure Canvas. |
| [Get Section](actions/get-section.md) | GET | Retrieves a section from Instructure Canvas. |
| [Get User Settings](actions/get-user-settings.md) | GET | Retrieves user settings from Instructure Canvas. |
| [Hide Stream Item](actions/hide-stream-item.md) | DELETE | Hides a stream item in Instructure Canvas. |
| [Initiate Page Views Query](actions/initiate-page-views-query.md) | POST | Initiates a page views query in Instructure Canvas. |
| [Initiate User File Upload](actions/initiate-user-file-upload.md) | POST | Initiates a user file upload in Instructure Canvas. |
| [List Avatar Options](actions/list-avatar-options.md) | GET | Retrieves avatar options from Instructure Canvas. |
| [List Course Sections](actions/list-course-sections.md) | GET | Retrieves course sections from Instructure Canvas. |
| [Remove Course Nickname](actions/remove-course-nickname.md) | DELETE | Deletes a course nickname from Instructure Canvas. |
| [Set Course Nickname](actions/set-course-nickname.md) | PUT | Sets a course nickname in Instructure Canvas. |
| [Update Custom Color](actions/update-custom-color.md) | PUT | Updates a custom color in Instructure Canvas. |
| [Update Dashboard Positions](actions/update-dashboard-positions.md) | PUT | Updates dashboard positions in Instructure Canvas. |
| [Update Files UI Version Preference](actions/update-files-ui-version-preference.md) | PUT | Updates the Files UI version preference in Instructure Canvas. |
| [Update Section](actions/update-section.md) | PUT | Updates an existing section in Instructure Canvas. |
| [Update Text Editor Preference](actions/update-text-editor-preference.md) | PUT | Updates the text editor preference in Instructure Canvas. |
| [Update User Settings](actions/update-user-settings.md) | PUT | Updates user settings in Instructure Canvas. |

### Unread Content Share Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Unread Content Share Count](actions/get-unread-content-share-count.md) | GET | Retrieves unread content share count from Instructure Canvas. |

### Unread Conversation Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Unread Conversation Count](actions/get-unread-conversation-count.md) | GET | Retrieves unread conversation count from Instructure Canvas. |

### Upcoming Event

| Action | Method | Description |
| --- | --- | --- |
| [List Upcoming Events](actions/list-upcoming-events.md) | GET | Retrieves upcoming events from Instructure Canvas. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Instructure Canvas. |
| [List Linked Observees](actions/list-linked-observees.md) | GET | Retrieves linked observees from Instructure Canvas. |
| [List Linked Observers](actions/list-linked-observers.md) | GET | Retrieves linked observers from Instructure Canvas. |

### User Colors

| Action | Method | Description |
| --- | --- | --- |
| [Get Custom Colors](actions/get-custom-colors.md) | GET | Retrieves custom colors from Instructure Canvas. |

### User Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User Profile](actions/get-current-user-profile.md) | GET | Retrieves the current user profile from Instructure Canvas. |

