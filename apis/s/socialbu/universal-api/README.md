# <img src="https://images.mindcloud.co/apps/icons/socialbu_1776779364223.png" alt="Socialbu logo" width="28" height="28"> Socialbu: Universal API

SocialBu helps teams create, schedule, publish, and manage social media content across connected accounts.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/socialbu/latest
- **Actions:** 49
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://socialbu.com/
- **Vendor API docs:** https://socialbu.com/developers/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (49)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Access Token](actions/get-access-token.md) | POST | Creates an access token for SocialBu API requests. |

### Account Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Accounts Metrics](actions/get-accounts-metrics.md) | GET | Retrieves account metrics from SocialBu insights. |

### Ai Tool

| Action | Method | Description |
| --- | --- | --- |
| [List AI Tools](actions/list-ai-tools.md) | GET | Retrieves available AI tools from SocialBu. |

### Ai Tool Result

| Action | Method | Description |
| --- | --- | --- |
| [Run AI Tool](actions/run-ai-tool.md) | POST | Runs an AI tool in SocialBu. |

### Automation Log

| Action | Method | Description |
| --- | --- | --- |
| [Get Automation Logs](actions/get-automation-logs.md) | GET | Retrieves automation logs from SocialBu insights. |

### Conversation Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Open Conversations Count](actions/get-open-conversations-count.md) | GET | Retrieves open conversation counts from SocialBu. |

### Curation Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Curation Item](actions/get-curation-item.md) | GET | Retrieves a curated content item by ID from SocialBu. |
| [List Curation Items](actions/list-curation-items.md) | GET | Retrieves curated content items from SocialBu. |

### Curation Topic

| Action | Method | Description |
| --- | --- | --- |
| [List Curation Topics](actions/list-curation-topics.md) | GET | Retrieves curation search suggestions from SocialBu. |

### Engagement Rate

| Action | Method | Description |
| --- | --- | --- |
| [Get Engagement Rate](actions/get-engagement-rate.md) | GET | Retrieves engagement rate from SocialBu insights. |

### Engagement Trend

| Action | Method | Description |
| --- | --- | --- |
| [Get Engagement Trend](actions/get-engagement-trend.md) | GET | Retrieves engagement trends from SocialBu insights. |

### Follower Growth

| Action | Method | Description |
| --- | --- | --- |
| [Get Followers Growth](actions/get-followers-growth.md) | GET | Retrieves follower growth from SocialBu insights. |

### Followers Insight

| Action | Method | Description |
| --- | --- | --- |
| [Get All Followers](actions/get-all-followers.md) | GET | Retrieves follower counts for SocialBu accounts. |

### Media Upload

| Action | Method | Description |
| --- | --- | --- |
| [Check Media Upload Status](actions/check-media-upload-status.md) | GET | Retrieves the status of a SocialBu media upload. |
| [Initiate Media Upload](actions/initiate-media-upload.md) | POST | Initiates a media upload to SocialBu. |
| [Upload Media by URL](actions/upload-media-by-url.md) | POST | Uploads media to SocialBu from a public URL. |

### Notification

| Action | Method | Description |
| --- | --- | --- |
| [Get Notification](actions/get-notification.md) | GET | Retrieves a notification by ID from SocialBu. |
| [List Notifications](actions/list-notifications.md) | GET | Retrieves notifications from SocialBu. |
| [List Unread Notifications](actions/list-unread-notifications.md) | GET | Retrieves unread notifications from SocialBu. |
| [Mark All Notifications as Read](actions/mark-all-notifications-as-read.md) | PUT | Marks all notifications as read in SocialBu. |
| [Mark Notification as Read](actions/mark-notification-as-read.md) | PUT | Marks a notification as read in SocialBu. |
| [Mark Notification as Unread](actions/mark-notification-as-unread.md) | PUT | Marks a notification as unread in SocialBu. |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Create Post](actions/create-post.md) | POST | Creates a new post in SocialBu. |
| [Delete Post](actions/delete-post.md) | DELETE | Deletes an existing post from SocialBu. |
| [Get Post](actions/get-post.md) | GET | Retrieves a post by ID from SocialBu. |
| [List Posts](actions/list-posts.md) | GET | Retrieves posts from SocialBu. |
| [Update Post](actions/update-post.md) | PUT | Updates an existing post in SocialBu. |

### Post Insights

| Action | Method | Description |
| --- | --- | --- |
| [Get Posts Counts](actions/get-posts-counts.md) | GET | Retrieves post counts from SocialBu insights. |

### Post Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Posts Metrics](actions/get-posts-metrics.md) | GET | Retrieves post metrics from SocialBu insights. |

### Post Supported Options

| Action | Method | Description |
| --- | --- | --- |
| [Get Supported Post Options](actions/get-supported-post-options.md) | GET | Retrieves supported posting options for SocialBu accounts. |

### Queue

| Action | Method | Description |
| --- | --- | --- |
| [List Queues](actions/list-queues.md) | GET | Retrieves publishing queues from SocialBu. |
| [Shuffle Queue](actions/shuffle-queue.md) | PUT | Shuffles posts in a SocialBu queue. |

### Queue Post

| Action | Method | Description |
| --- | --- | --- |
| [Add Post to Queue](actions/add-post-to-queue.md) | POST | Adds a post to a specific SocialBu queue. |
| [List Queue Posts](actions/list-queue-posts.md) | GET | Retrieves posts in a specific SocialBu queue. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Logout](actions/logout.md) | DELETE | Deletes the current SocialBu access token. |

### Social Account

| Action | Method | Description |
| --- | --- | --- |
| [Connect Account](actions/connect-account.md) | POST | Connects a new social account to SocialBu. |
| [Delete Account](actions/delete-account.md) | DELETE | Deletes an existing social account from SocialBu. |
| [Get Account](actions/get-account.md) | GET | Retrieves a social account by ID from SocialBu. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves social accounts from SocialBu. |
| [Update Account](actions/update-account.md) | PUT | Updates an existing social account in SocialBu. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Create Team](actions/create-team.md) | POST | Creates a new team in SocialBu. |
| [Delete Team](actions/delete-team.md) | DELETE | Deletes an existing team from SocialBu. |
| [List Teams](actions/list-teams.md) | GET | Retrieves teams from SocialBu. |
| [Update Team](actions/update-team.md) | PUT | Updates an existing team in SocialBu. |

### Team Activity

| Action | Method | Description |
| --- | --- | --- |
| [Get Team Activity](actions/get-team-activity.md) | GET | Retrieves team activity logs from SocialBu insights. |

### Team Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Team Metrics](actions/get-team-metrics.md) | GET | Retrieves team metrics from SocialBu insights. |

### Top Post

| Action | Method | Description |
| --- | --- | --- |
| [Get Top Posts](actions/get-top-posts.md) | GET | Retrieves top-performing posts from SocialBu insights. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |

### User Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get User Stats](actions/get-user-stats.md) | GET | Retrieves user stats from SocialBu insights. |

