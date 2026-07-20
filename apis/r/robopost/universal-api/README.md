# <img src="https://images.mindcloud.co/apps/icons/robopost_1775084072773.png" alt="Robopost logo" width="28" height="28"> Robopost: Universal API

Robopost helps teams create, schedule, publish, and automate social media content across channels.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/robopost/latest
- **Category:** Marketing / Social Media
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://robopost.app/
- **Vendor API docs:** https://robopost.app/docs/robopost-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate API Key](actions/validate-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/robopost/latest/actions/validate-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Aggregated Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Aggregated Analytics by ID](actions/get-aggregated-analytics-by-id.md) | GET | Retrieves aggregated analytics from Robopost by ID. |
| [List Aggregated Analytics](actions/list-aggregated-analytics.md) | GET | Retrieves aggregated analytics from Robopost. |

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [List Channels](actions/list-channels.md) | GET | Retrieves channels from Robopost. |

### Health Check

| Action | Method | Description |
| --- | --- | --- |
| [Ping](actions/ping.md) | GET | Retrieves health check status from Robopost. |

### Media

| Action | Method | Description |
| --- | --- | --- |
| [Upload Media](actions/upload-media.md) | POST | Uploads media to Robopost. |

### Post Collection

| Action | Method | Description |
| --- | --- | --- |
| [List Post Collections](actions/list-post-collections.md) | GET | Retrieves post collections from Robopost. |

### Scheduled Post

| Action | Method | Description |
| --- | --- | --- |
| [Create Scheduled Posts](actions/create-scheduled-posts.md) | POST | Creates scheduled posts in Robopost. |

### Social Inbox Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Social Inbox Item](actions/get-social-inbox-item.md) | GET | Retrieves a social inbox item from Robopost. |
| [List Social Inbox Items](actions/list-social-inbox-items.md) | GET | Retrieves social inbox items from Robopost. |

### Social Inbox Thread

| Action | Method | Description |
| --- | --- | --- |
| [List GMB Threads for One Channel](actions/list-gmb-threads-for-one-channel.md) | GET | Retrieves Google Business threads for one Robopost channel. |
| [List Social Inbox Threads Grouped by Post](actions/list-social-inbox-threads-grouped-by-post.md) | GET | Retrieves social inbox threads grouped by post from Robopost. |

### Social Inbox Unread Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Unread Count](actions/get-unread-count.md) | GET | Retrieves the unread inbox count from Robopost. |

### Social Inbox Unread Counts By Channel

| Action | Method | Description |
| --- | --- | --- |
| [Get Unread Count by Channel](actions/get-unread-count-by-channel.md) | GET | Retrieves unread inbox counts by channel from Robopost. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Validate API Key](actions/validate-api-key.md) | GET | Retrieves API key validation details from Robopost. |

### Video Series

| Action | Method | Description |
| --- | --- | --- |
| [Create Video Series](actions/create-video-series.md) | POST | Creates a video series in Robopost. |
| [Delete Video Series](actions/delete-video-series.md) | DELETE | Deletes an existing video series from Robopost. |
| [Get Video Series](actions/get-video-series.md) | GET | Retrieves a video series from Robopost. |
| [List Video Series](actions/list-video-series.md) | GET | Retrieves video series from Robopost. |
| [Update Video Series](actions/update-video-series.md) | PUT | Updates an existing video series in Robopost. |

### Video Task

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Video Task](actions/cancel-video-task.md) | DELETE | Deletes an existing video task from Robopost. |
| [Create Video Generation Task](actions/create-video-generation-task.md) | POST | Creates a video generation task in Robopost. |
| [Get Video Task](actions/get-video-task.md) | GET | Retrieves a video task from Robopost. |
| [Get Video Task Details](actions/get-video-task-details.md) | GET | Retrieves video task details from Robopost. |
| [List Video Tasks](actions/list-video-tasks.md) | GET | Retrieves video tasks from Robopost. |

