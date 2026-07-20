# <img src="https://images.mindcloud.co/apps/icons/loomio_1775166158898.png" alt="Loomio logo" width="28" height="28"> Loomio: Universal API

Loomio is a collaborative decision-making platform for discussions, polls, groups, documents, and governance workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/loomio/latest
- **Category:** Productivity / Project Management
- **Actions:** 33
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.loomio.com
- **Vendor API docs:** https://github.com/loomio/loomio/tree/master/app/controllers/api/v1

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Groups](actions/list-groups.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loomio/latest/actions/list-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (33)

### Announcements

| Action | Method | Description |
| --- | --- | --- |
| [Count Announcements](actions/count-announcements.md) | GET | Counts announcements in Loomio. |
| [List Announcement History](actions/list-announcement-history.md) | GET | Retrieves announcement history from Loomio. |
| [Search Announcements](actions/search-announcements.md) | GET | Finds announcements in Loomio by search query. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [List Discussion Documents](actions/list-discussion-documents.md) | GET | Retrieves documents from a Loomio discussion. |
| [List Group Documents](actions/list-group-documents.md) | GET | Retrieves documents from a Loomio group. |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Check Email Exists](actions/check-email-exists.md) | GET | Checks whether an email exists in Loomio. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Count Discussion Events](actions/count-discussion-events.md) | GET | Counts discussion events in Loomio. |
| [List Discussion Events](actions/list-discussion-events.md) | GET | Retrieves discussion events from Loomio. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [List Discussion Position Keys](actions/list-discussion-position-keys.md) | GET | Retrieves discussion position keys from Loomio. |
| [List Discussion Timeline Events](actions/list-discussion-timeline-events.md) | GET | Retrieves discussion timeline events from Loomio. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from Loomio. |
| [List Group Subgroups](actions/list-group-subgroups.md) | GET | Retrieves subgroups from a Loomio group. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from Loomio. |
| [List Profile Groups](actions/list-profile-groups.md) | GET | Retrieves profile groups from Loomio. |
| [Suggest Group Handle](actions/suggest-group-handle.md) | GET | Retrieves a suggested group handle from Loomio. |

### Membership

| Action | Method | Description |
| --- | --- | --- |
| [List Group Memberships](actions/list-group-memberships.md) | GET | Retrieves group memberships from Loomio. |
| [List My Memberships](actions/list-my-memberships.md) | GET | Retrieves your memberships from Loomio. |

### Notifications

| Action | Method | Description |
| --- | --- | --- |
| [List Notifications](actions/list-notifications.md) | GET | Retrieves notifications from Loomio. |

### Proposals

| Action | Method | Description |
| --- | --- | --- |
| [Get Poll](actions/get-poll.md) | GET | Retrieves a poll from Loomio. |
| [List Poll Receipts](actions/list-poll-receipts.md) | GET | Retrieves poll receipts from Loomio. |
| [List Poll Voters](actions/list-poll-voters.md) | GET | Retrieves poll voters from Loomio. |
| [List Polls](actions/list-polls.md) | GET | Retrieves polls from Loomio. |

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [Search Loomio](actions/search-loomio.md) | GET | Finds results in Loomio by search query. |

### Reactions

| Action | Method | Description |
| --- | --- | --- |
| [List Reactions](actions/list-reactions.md) | GET | Retrieves reactions from Loomio. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Count Explore Results](actions/count-explore-results.md) | GET | Counts explore results in Loomio. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from Loomio. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Browse Discussion Templates](actions/browse-discussion-templates.md) | GET | Retrieves discussion templates from Loomio. |
| [Browse Poll Templates](actions/browse-poll-templates.md) | GET | Retrieves poll templates from Loomio. |

### Threads

| Action | Method | Description |
| --- | --- | --- |
| [Get Discussion](actions/get-discussion.md) | GET | Retrieves a discussion from Loomio. |
| [List Direct Discussions](actions/list-direct-discussions.md) | GET | Retrieves direct discussions from Loomio. |
| [List Discussions](actions/list-discussions.md) | GET | Retrieves discussions from Loomio. |

### Timezone Setting

| Action | Method | Description |
| --- | --- | --- |
| [List All Time Zones](actions/list-all-time-zones.md) | GET | Retrieves all time zones from Loomio. |
| [List Time Zones](actions/list-time-zones.md) | GET | Retrieves time zones from Loomio. |

