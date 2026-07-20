# Instructure: Native API Reference

A consolidated summary of Instructure's API configuration and 115 documented operations, with links to official documentation.

- **Official docs:** https://developerdocs.instructure.com/services/canvas
- **API base URL:** `https://canvas.instructure.com/api/v1`

## Authentication

### Canvas API Token

Use a Canvas access token for a user account. MindCloud sends it as Authorization: Bearer <token>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developerdocs.instructure.com/services/canvas/oauth2/file.oauth)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 25; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (115 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Course To Favorites](actions/add-course-to-favorites.md) | `POST /users/self/favorites/courses/:id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/favorites) |
| [Add Group To Favorites](actions/add-group-to-favorites.md) | `POST /users/self/favorites/groups/:id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/favorites) |
| [Clear Course Nicknames](actions/clear-course-nicknames.md) | `DELETE /users/self/course_nicknames` | [docs](https://developerdocs.instructure.com/services/canvas/resources/users) |
| [Create Assignment](actions/create-assignment.md) | `POST /courses/:course_id/assignments` | [docs](https://developerdocs.instructure.com/services/canvas/resources/assignments#method.assignments_api.create) |
| [Create Bookmark](actions/create-bookmark.md) | `POST /users/self/bookmarks` | [docs](https://developerdocs.instructure.com/services/canvas/resources/bookmarks) |
| [Create Calendar Event](actions/create-calendar-event.md) | `POST /calendar_events` | [docs](https://developerdocs.instructure.com/services/canvas/resources/calendar_events#method.calendar_events_api.create) |
| [Create Course Section](actions/create-course-section.md) | `POST /courses/:course_id/sections` | [docs](https://developerdocs.instructure.com/services/canvas/resources/sections#method.sections.create) |
| [Create Discussion Topic](actions/create-discussion-topic.md) | `POST /courses/:course_id/discussion_topics` | [docs](https://developerdocs.instructure.com/services/canvas/resources/discussion_topics#method.discussion_topics.create) |
| [Create Folder](actions/create-folder.md) | `POST /folders/:parent_folder_id/folders` | [docs](https://developerdocs.instructure.com/services/canvas/resources/files#method.folders.create) |
| [Create Page](actions/create-page.md) | `POST /courses/:course_id/pages` | [docs](https://developerdocs.instructure.com/services/canvas/resources/pages#method.wiki_pages_api.create) |
| [Create Planner Note](actions/create-planner-note.md) | `POST /planner_notes` | [docs](https://developerdocs.instructure.com/services/canvas/resources/planner) |
| [Create Planner Override](actions/create-planner-override.md) | `POST /planner/overrides` | [docs](https://developerdocs.instructure.com/services/canvas/resources/planner) |
| [Delete Assignment](actions/delete-assignment.md) | `DELETE /courses/:course_id/assignments/:assignment_id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/assignments#method.assignments.destroy) |
| [Delete Bookmark](actions/delete-bookmark.md) | `DELETE /users/self/bookmarks/:bookmark_id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/bookmarks) |
| [Delete Calendar Event](actions/delete-calendar-event.md) | `DELETE /calendar_events/:event_id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/calendar_events#method.calendar_events_api.destroy) |
| [Delete Discussion Topic](actions/delete-discussion-topic.md) | `DELETE /courses/:course_id/discussion_topics/:topic_id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/discussion_topics#method.discussion_topics.destroy) |
| [Delete File](actions/delete-file.md) | `DELETE /files/:id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/files#method.files.destroy) |
| [Delete Folder](actions/delete-folder.md) | `DELETE /folders/:folder_id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/files#method.folders.api_destroy) |
| [Delete Page](actions/delete-page.md) | `DELETE /courses/:course_id/pages/:page_id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/pages#method.wiki_pages_api.destroy) |
| [Delete Planner Note](actions/delete-planner-note.md) | `DELETE /planner_notes/:id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/planner) |
| [Delete Planner Override](actions/delete-planner-override.md) | `DELETE /planner/overrides/:id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/planner) |
| [Delete Section](actions/delete-section.md) | `DELETE /sections/:id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/sections#method.sections.destroy) |
| [Get Activity Stream Summary](actions/get-activity-stream-summary.md) | `GET /users/self/activity_stream/summary` | [docs](https://developerdocs.instructure.com/services/canvas/resources/users#method.users.activity_stream_summary) |
| [Get Assignment](actions/get-assignment.md) | `GET /courses/:course_id/assignments/:assignment_id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/assignments#method.assignments_api.show) |
| [Get Bookmark](actions/get-bookmark.md) | `GET /users/self/bookmarks/:bookmark_id` | [docs](https://developerdocs.instructure.com/services/canvas/file.all_resources/bookmarks) |
| [Get Calendar Event](actions/get-calendar-event.md) | `GET /calendar_events/:event_id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/calendar_events#method.calendar_events_api.show) |
| [Get Conversation Batches](actions/get-conversation-batches.md) | `GET /conversations/batches` | [docs](https://developerdocs.instructure.com/services/canvas/resources/conversations) |
| [Get Course](actions/get-course.md) | `GET /courses/:course_id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/courses#method.courses.show) |
| [Get Course Nickname](actions/get-course-nickname.md) | `GET /users/self/course_nicknames/:course_id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/users#method.coursenicknames.show) |
| [Get Current User](actions/get-current-user.md) | `GET /users/self` | [docs](https://developerdocs.instructure.com/services/canvas/resources/users#method.users.api_show) |
| [Get Current User Profile](actions/get-current-user-profile.md) | `GET /users/self/profile` | [docs](https://developerdocs.instructure.com/services/canvas/resources/users#method.profile.settings) |
| [Get Custom Color](actions/get-custom-color.md) | `GET /users/self/colors/:asset_string` | [docs](https://developerdocs.instructure.com/services/canvas/resources/users#method.users.get_custom_color) |
| [Get Custom Colors](actions/get-custom-colors.md) | `GET /users/self/colors` | [docs](https://developerdocs.instructure.com/services/canvas/resources/users#method.users.get_custom_colors) |
| [Get Dashboard Positions](actions/get-dashboard-positions.md) | `GET /users/self/dashboard_positions` | [docs](https://developerdocs.instructure.com/services/canvas/resources/users) |
| [Get Discussion Topic](actions/get-discussion-topic.md) | `GET /courses/:course_id/discussion_topics/:topic_id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/discussion_topics#method.discussion_topics_api.show) |
| [Get Enrollment](actions/get-enrollment.md) | `GET /courses/:course_id/enrollments/:enrollment_id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/enrollments#method.enrollments_api.show) |
| [Get File](actions/get-file.md) | `GET /files/:file_id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/files#method.files.api_show) |
| [Get File Public Preview URL](actions/get-file-public-preview-url.md) | `GET /files/:id/public_url` | [docs](https://developerdocs.instructure.com/services/canvas/resources/files#method.files.public_url) |
| [Get Folder](actions/get-folder.md) | `GET /folders/:folder_id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/files#method.folders.show) |
| [Get Graded Submissions](actions/get-graded-submissions.md) | `GET /users/self/graded_submissions` | [docs](https://developerdocs.instructure.com/services/canvas/resources/users#method.users.user_graded_submissions) |
| [Get Module](actions/get-module.md) | `GET /courses/:course_id/modules/:module_id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/modules#method.context_modules_api.show) |
| [Get Notification Preference](actions/get-notification-preference.md) | `GET /users/self/communication_channels/:communication_channel_id/notification_preferences/:notification` | [docs](https://developerdocs.instructure.com/services/canvas/resources/notification_preferences) |
| [Get Page](actions/get-page.md) | `GET /courses/:course_id/pages/:page_id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/pages#method.wiki_pages_api.show) |
| [Get Page Views Query Status](actions/get-page-views-query-status.md) | `GET /users/self/page_views/query/:query_id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/users#method.page_views.show) |
| [Get Planner Note](actions/get-planner-note.md) | `GET /planner_notes/:id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/planner) |
| [Get Planner Override](actions/get-planner-override.md) | `GET /planner/overrides/:id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/planner) |
| [Get Section](actions/get-section.md) | `GET /courses/:course_id/sections/:id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/sections#method.sections.show) |
| [Get Todo Item Count](actions/get-todo-item-count.md) | `GET /users/self/todo_item_count` | [docs](https://developerdocs.instructure.com/services/canvas/resources/users#method.users.todo_item_count) |
| [Get Unread Content Share Count](actions/get-unread-content-share-count.md) | `GET /users/self/content_shares/unread_count` | [docs](https://developerdocs.instructure.com/services/canvas/resources/content_shares) |
| [Get Unread Conversation Count](actions/get-unread-conversation-count.md) | `GET /conversations/unread_count` | [docs](https://developerdocs.instructure.com/services/canvas/resources/conversations) |
| [Get User Settings](actions/get-user-settings.md) | `GET /users/self/settings` | [docs](https://developerdocs.instructure.com/services/canvas/resources/users#method.users.settings) |
| [Hide All Stream Items](actions/hide-all-stream-items.md) | `DELETE /users/self/activity_stream` | [docs](https://developerdocs.instructure.com/services/canvas/resources/users) |
| [Hide Stream Item](actions/hide-stream-item.md) | `DELETE /users/self/activity_stream/:id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/users#method.users.ignore_stream_item) |
| [Initiate Page Views Query](actions/initiate-page-views-query.md) | `POST /users/self/page_views/query` | [docs](https://developerdocs.instructure.com/services/canvas/resources/users#method.page_views.query) |
| [Initiate User File Upload](actions/initiate-user-file-upload.md) | `POST /users/self/files` | [docs](https://developerdocs.instructure.com/services/canvas/resources/users#method.users.create_file) |
| [List Activity Stream](actions/list-activity-stream.md) | `GET /users/self/activity_stream` | [docs](https://developerdocs.instructure.com/services/canvas/resources/users#method.users.activity_stream) |
| [List Announcements](actions/list-announcements.md) | `GET /announcements` | [docs](https://developerdocs.instructure.com/services/canvas/resources/announcements#method.announcements_api.index) |
| [List Assignments](actions/list-assignments.md) | `GET /courses/:course_id/assignments` | [docs](https://developerdocs.instructure.com/services/canvas/resources/assignments#method.assignments_api.index) |
| [List Avatar Options](actions/list-avatar-options.md) | `GET /users/self/avatars` | [docs](https://developerdocs.instructure.com/services/canvas/resources/users#method.profile.profile_pics) |
| [List Bookmarks](actions/list-bookmarks.md) | `GET /users/self/bookmarks` | [docs](https://developerdocs.instructure.com/services/canvas/file.all_resources/bookmarks) |
| [List Calendar Events](actions/list-calendar-events.md) | `GET /calendar_events` | [docs](https://developerdocs.instructure.com/services/canvas/resources/calendar_events#method.calendar_events_api.index) |
| [List Communication Channels](actions/list-communication-channels.md) | `GET /users/self/communication_channels` | [docs](https://developerdocs.instructure.com/services/canvas/resources/communication_channels) |
| [List Conversations](actions/list-conversations.md) | `GET /conversations` | [docs](https://developerdocs.instructure.com/services/canvas/resources/conversations) |
| [List Course Enrollments](actions/list-course-enrollments.md) | `GET /courses/:course_id/enrollments` | [docs](https://developerdocs.instructure.com/services/canvas/resources/enrollments#method.enrollments_api.index) |
| [List Course Nicknames](actions/list-course-nicknames.md) | `GET /users/self/course_nicknames` | [docs](https://developerdocs.instructure.com/services/canvas/resources/users) |
| [List Course Sections](actions/list-course-sections.md) | `GET /courses/:course_id/sections` | [docs](https://developerdocs.instructure.com/services/canvas/resources/sections#method.sections.index) |
| [List Courses](actions/list-courses.md) | `GET /courses` | [docs](https://developerdocs.instructure.com/services/canvas/resources/courses#method.courses.index) |
| [List Discussion Topics](actions/list-discussion-topics.md) | `GET /courses/:course_id/discussion_topics` | [docs](https://developerdocs.instructure.com/services/canvas/resources/discussion_topics#method.discussion_topics.index) |
| [List Favorite Courses](actions/list-favorite-courses.md) | `GET /users/self/favorites/courses` | [docs](https://developerdocs.instructure.com/services/canvas/resources/favorites) |
| [List Favorite Groups](actions/list-favorite-groups.md) | `GET /users/self/favorites/groups` | [docs](https://developerdocs.instructure.com/services/canvas/resources/favorites) |
| [List Folder Files](actions/list-folder-files.md) | `GET /folders/:folder_id/files` | [docs](https://developerdocs.instructure.com/services/canvas/resources/files#method.files.api_index) |
| [List Linked Observees](actions/list-linked-observees.md) | `GET /users/self/observees` | [docs](https://developerdocs.instructure.com/services/canvas/resources/user_observees) |
| [List Linked Observers](actions/list-linked-observers.md) | `GET /users/self/observers` | [docs](https://developerdocs.instructure.com/services/canvas/resources/user_observees) |
| [List Missing Submissions](actions/list-missing-submissions.md) | `GET /users/self/missing_submissions` | [docs](https://developerdocs.instructure.com/services/canvas/resources/users#method.users.missing_submissions) |
| [List Module Items](actions/list-module-items.md) | `GET /courses/:course_id/modules/:module_id/items` | [docs](https://developerdocs.instructure.com/services/canvas/resources/modules#method.context_module_items_api.index) |
| [List Modules](actions/list-modules.md) | `GET /courses/:course_id/modules` | [docs](https://developerdocs.instructure.com/services/canvas/resources/modules#method.context_modules_api.index) |
| [List Notification Preference Categories](actions/list-notification-preference-categories.md) | `GET /users/self/communication_channels/:communication_channel_id/notification_preference_categories` | [docs](https://developerdocs.instructure.com/services/canvas/resources/notification_preferences) |
| [List Notification Preferences](actions/list-notification-preferences.md) | `GET /users/self/communication_channels/:communication_channel_id/notification_preferences` | [docs](https://developerdocs.instructure.com/services/canvas/resources/notification_preferences) |
| [List Page Views](actions/list-page-views.md) | `GET /users/self/page_views` | [docs](https://developerdocs.instructure.com/services/canvas/resources/users) |
| [List Pages](actions/list-pages.md) | `GET /courses/:course_id/pages` | [docs](https://developerdocs.instructure.com/services/canvas/resources/pages#method.wiki_pages_api.index) |
| [List Planner Items](actions/list-planner-items.md) | `GET /planner/items` | [docs](https://developerdocs.instructure.com/services/canvas/resources/planner) |
| [List Planner Notes](actions/list-planner-notes.md) | `GET /planner_notes` | [docs](https://developerdocs.instructure.com/services/canvas/resources/planner) |
| [List Planner Overrides](actions/list-planner-overrides.md) | `GET /planner/overrides` | [docs](https://developerdocs.instructure.com/services/canvas/resources/planner) |
| [List Received Content Shares](actions/list-received-content-shares.md) | `GET /users/self/content_shares/received` | [docs](https://developerdocs.instructure.com/services/canvas/resources/content_shares) |
| [List Sent Content Shares](actions/list-sent-content-shares.md) | `GET /users/self/content_shares/sent` | [docs](https://developerdocs.instructure.com/services/canvas/resources/content_shares) |
| [List Todo Items](actions/list-todo-items.md) | `GET /users/self/todo` | [docs](https://developerdocs.instructure.com/services/canvas/resources/users#method.users.todo_items) |
| [List Upcoming Events](actions/list-upcoming-events.md) | `GET /users/self/upcoming_events` | [docs](https://developerdocs.instructure.com/services/canvas/resources/users#method.users.upcoming_events) |
| [List User Files](actions/list-user-files.md) | `GET /users/self/files` | [docs](https://developerdocs.instructure.com/services/canvas/resources/files#method.files.api_index) |
| [List User Folders](actions/list-user-folders.md) | `GET /users/self/folders` | [docs](https://developerdocs.instructure.com/services/canvas/resources/files#method.folders.list_all_folders) |
| [List User Groups](actions/list-user-groups.md) | `GET /users/self/groups` | [docs](https://developerdocs.instructure.com/services/canvas/resources/groups) |
| [Mark All Conversations As Read](actions/mark-all-conversations-as-read.md) | `POST /conversations/mark_all_as_read` | [docs](https://developerdocs.instructure.com/services/canvas/resources/conversations) |
| [Remove Course From Favorites](actions/remove-course-from-favorites.md) | `DELETE /users/self/favorites/courses/:id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/favorites) |
| [Remove Course Nickname](actions/remove-course-nickname.md) | `DELETE /users/self/course_nicknames/:course_id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/users#method.coursenicknames.delete) |
| [Remove Group From Favorites](actions/remove-group-from-favorites.md) | `DELETE /users/self/favorites/groups/:id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/favorites) |
| [Reset Course Favorites](actions/reset-course-favorites.md) | `DELETE /users/self/favorites/courses` | [docs](https://developerdocs.instructure.com/services/canvas/resources/favorites) |
| [Reset Group Favorites](actions/reset-group-favorites.md) | `DELETE /users/self/favorites/groups` | [docs](https://developerdocs.instructure.com/services/canvas/resources/favorites) |
| [Set Course Nickname](actions/set-course-nickname.md) | `PUT /users/self/course_nicknames/:course_id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/users#method.coursenicknames.update) |
| [Update Assignment](actions/update-assignment.md) | `PUT /courses/:course_id/assignments/:assignment_id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/assignments#method.assignments_api.update) |
| [Update Bookmark](actions/update-bookmark.md) | `PUT /users/self/bookmarks/:bookmark_id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/bookmarks) |
| [Update Calendar Event](actions/update-calendar-event.md) | `PUT /calendar_events/:event_id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/calendar_events#method.calendar_events_api.update) |
| [Update Custom Color](actions/update-custom-color.md) | `PUT /users/self/colors/:asset_string` | [docs](https://developerdocs.instructure.com/services/canvas/resources/users#method.users.set_custom_color) |
| [Update Dashboard Positions](actions/update-dashboard-positions.md) | `PUT /users/self/dashboard_positions` | [docs](https://developerdocs.instructure.com/services/canvas/resources/users#method.users.set_dashboard_positions) |
| [Update Discussion Topic](actions/update-discussion-topic.md) | `PUT /courses/:course_id/discussion_topics/:topic_id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/discussion_topics#method.discussion_topics.update) |
| [Update File](actions/update-file.md) | `PUT /files/:id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/files#method.files.api_update) |
| [Update Files UI Version Preference](actions/update-files-ui-version-preference.md) | `PUT /users/self/files_ui_version_preference` | [docs](https://developerdocs.instructure.com/services/canvas/resources/users#method.users.set_files_ui_version_preference) |
| [Update Folder](actions/update-folder.md) | `PUT /folders/:folder_id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/files#method.folders.update) |
| [Update Multiple Notification Preferences](actions/update-multiple-notification-preferences.md) | `PUT /users/self/communication_channels/:communication_channel_id/notification_preferences` | [docs](https://developerdocs.instructure.com/services/canvas/resources/notification_preferences) |
| [Update Notification Preference](actions/update-notification-preference.md) | `PUT /users/self/communication_channels/:communication_channel_id/notification_preferences/:notification` | [docs](https://developerdocs.instructure.com/services/canvas/resources/notification_preferences) |
| [Update Notification Preferences By Category](actions/update-notification-preferences-by-category.md) | `PUT /users/self/communication_channels/:communication_channel_id/notification_preference_categories/:category` | [docs](https://developerdocs.instructure.com/services/canvas/resources/notification_preferences) |
| [Update Page](actions/update-page.md) | `PUT /courses/:course_id/pages/:page_id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/pages#method.wiki_pages_api.update) |
| [Update Planner Note](actions/update-planner-note.md) | `PUT /planner_notes/:id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/planner) |
| [Update Planner Override](actions/update-planner-override.md) | `PUT /planner/overrides/:id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/planner) |
| [Update Section](actions/update-section.md) | `PUT /sections/:id` | [docs](https://developerdocs.instructure.com/services/canvas/resources/sections#method.sections.update) |
| [Update Text Editor Preference](actions/update-text-editor-preference.md) | `PUT /users/self/text_editor_preference` | [docs](https://developerdocs.instructure.com/services/canvas/resources/users#method.users.set_text_editor_preference) |
| [Update User Settings](actions/update-user-settings.md) | `PUT /users/self/settings` | [docs](https://developerdocs.instructure.com/services/canvas/resources/users#method.users.settings) |
