# Loomio: Native API Reference

A consolidated summary of Loomio's API configuration and 33 documented operations, with links to official documentation.

- **Official docs:** https://github.com/loomio/loomio/tree/master/app/controllers/api/v1
- **API base URL:** `https://www.loomio.com/api/v1`

## Authentication

### API Key

Authenticate Loomio requests with a shared api_key parameter.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.loomio.com/help/api2)

## Endpoints (33 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Browse Discussion Templates](actions/browse-discussion-templates.md) | `GET /discussion_templates/browse` | [docs](https://github.com/loomio/loomio/blob/master/config/routes.rb) |
| [Browse Poll Templates](actions/browse-poll-templates.md) | `GET /poll_templates/browse` | [docs](https://github.com/loomio/loomio/blob/master/config/routes.rb) |
| [Check Email Exists](actions/check-email-exists.md) | `GET /profile/email_exists` | [docs](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/profile_controller.rb) |
| [Count Announcements](actions/count-announcements.md) | `GET /announcements/count` | [docs](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/announcements_controller.rb) |
| [Count Discussion Events](actions/count-discussion-events.md) | `GET /events/count` | [docs](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/events_controller.rb) |
| [Count Explore Results](actions/count-explore-results.md) | `GET /groups/count_explore_results` | [docs](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/groups_controller.rb) |
| [Get Discussion](actions/get-discussion.md) | `GET /discussions/:id` | [docs](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/discussions_controller.rb) |
| [Get Group](actions/get-group.md) | `GET /groups/:id` | [docs](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/groups_controller.rb) |
| [Get Poll](actions/get-poll.md) | `GET /polls/:id` | [docs](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/polls_controller.rb) |
| [List All Time Zones](actions/list-all-time-zones.md) | `GET /profile/all_time_zones` | [docs](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/profile_controller.rb) |
| [List Announcement History](actions/list-announcement-history.md) | `GET /announcements/history` | [docs](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/announcements_controller.rb) |
| [List Direct Discussions](actions/list-direct-discussions.md) | `GET /discussions/direct` | [docs](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/discussions_controller.rb) |
| [List Discussion Documents](actions/list-discussion-documents.md) | `GET /documents/for_discussion` | [docs](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/documents_controller.rb) |
| [List Discussion Events](actions/list-discussion-events.md) | `GET /events` | [docs](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/events_controller.rb) |
| [List Discussion Position Keys](actions/list-discussion-position-keys.md) | `GET /events/position_keys` | [docs](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/events_controller.rb) |
| [List Discussion Timeline Events](actions/list-discussion-timeline-events.md) | `GET /events/timeline` | [docs](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/events_controller.rb) |
| [List Discussions](actions/list-discussions.md) | `GET /discussions` | [docs](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/discussions_controller.rb) |
| [List Group Documents](actions/list-group-documents.md) | `GET /documents/for_group` | [docs](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/documents_controller.rb) |
| [List Group Memberships](actions/list-group-memberships.md) | `GET /memberships` | [docs](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/memberships_controller.rb) |
| [List Group Subgroups](actions/list-group-subgroups.md) | `GET /groups/:id/subgroups` | [docs](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/groups_controller.rb) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/groups_controller.rb) |
| [List My Memberships](actions/list-my-memberships.md) | `GET /memberships/my_memberships` | [docs](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/memberships_controller.rb) |
| [List Notifications](actions/list-notifications.md) | `GET /notifications` | [docs](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/notifications_controller.rb) |
| [List Poll Receipts](actions/list-poll-receipts.md) | `GET /polls/:id/receipts` | [docs](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/polls_controller.rb) |
| [List Poll Voters](actions/list-poll-voters.md) | `GET /polls/:id/voters` | [docs](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/polls_controller.rb) |
| [List Polls](actions/list-polls.md) | `GET /polls` | [docs](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/polls_controller.rb) |
| [List Profile Groups](actions/list-profile-groups.md) | `GET /profile/groups` | [docs](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/profile_controller.rb) |
| [List Reactions](actions/list-reactions.md) | `GET /reactions` | [docs](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/reactions_controller.rb) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/tasks_controller.rb) |
| [List Time Zones](actions/list-time-zones.md) | `GET /profile/time_zones` | [docs](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/profile_controller.rb) |
| [Search Announcements](actions/search-announcements.md) | `GET /announcements/search` | [docs](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/announcements_controller.rb) |
| [Search Loomio](actions/search-loomio.md) | `GET /search` | [docs](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/search_controller.rb) |
| [Suggest Group Handle](actions/suggest-group-handle.md) | `GET /groups/suggest_handle` | [docs](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/groups_controller.rb) |
