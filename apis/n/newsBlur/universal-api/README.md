# <img src="https://images.mindcloud.co/apps/icons/news-blur_1777903872777.png" alt="NewsBlur logo" width="28" height="28"> NewsBlur: Universal API

NewsBlur is a personal news reader for following RSS feeds, reading unread stories, saving articles, and managing feed subscriptions.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/newsBlur/latest
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.newsblur.com
- **Vendor API docs:** https://newsblur.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Autocomplete Feeds](actions/autocomplete-feeds.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/autocomplete-feeds?connectionId=$CONNECTION_ID&term=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Favicon

| Action | Method | Description |
| --- | --- | --- |
| [List Favicons](actions/list-favicons.md) | GET | Retrieves feed favicons from NewsBlur. |

### Feed

| Action | Method | Description |
| --- | --- | --- |
| [Add Feed](actions/add-feed.md) | POST | Adds a feed to NewsBlur. |
| [Autocomplete Feeds](actions/autocomplete-feeds.md) | GET | Finds feeds in NewsBlur by search phrase. |
| [List Feeds](actions/list-feeds.md) | GET | Retrieves subscribed feeds from NewsBlur. |
| [Mark Feeds As Read](actions/mark-feeds-as-read.md) | PUT | Marks feeds as read in NewsBlur. |
| [Search Feed](actions/search-feed.md) | GET | Finds a feed in NewsBlur by website or RSS address. |

### Feed Count

| Action | Method | Description |
| --- | --- | --- |
| [Refresh Feed Counts](actions/refresh-feed-counts.md) | GET | Retrieves unread feed counts from NewsBlur. |

### Feed Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Feed Page](actions/get-feed-page.md) | GET | Retrieves a feed page from NewsBlur. |

### Feed Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Feed Statistics](actions/get-feed-statistics.md) | GET | Retrieves feed statistics from NewsBlur. |

### Feed Trainer

| Action | Method | Description |
| --- | --- | --- |
| [List Feed Trainers](actions/list-feed-trainers.md) | GET | Retrieves feed classifiers from NewsBlur. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Add Folder](actions/add-folder.md) | POST | Creates a folder in NewsBlur. |

### Read Story

| Action | Method | Description |
| --- | --- | --- |
| [List Read Stories](actions/list-read-stories.md) | GET | Retrieves read stories from NewsBlur. |

### Saved Story

| Action | Method | Description |
| --- | --- | --- |
| [List Starred Stories](actions/list-starred-stories.md) | GET | Retrieves starred stories from NewsBlur. |
| [Save Story](actions/save-story.md) | PUT | Saves a story in NewsBlur. |
| [Unsave Story](actions/unsave-story.md) | PUT | Removes a saved story from NewsBlur. |

### Saved Story Hash

| Action | Method | Description |
| --- | --- | --- |
| [List Starred Story Hashes](actions/list-starred-story-hashes.md) | GET | Retrieves starred story hashes from NewsBlur. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Log In](actions/log-in.md) | POST | Creates a session in NewsBlur. |

### Story

| Action | Method | Description |
| --- | --- | --- |
| [Get Feed Stories](actions/get-feed-stories.md) | GET | Retrieves stories from a feed in NewsBlur. |
| [Get Original Story](actions/get-original-story.md) | GET | Retrieves a story's original webpage from NewsBlur. |
| [Get River Stories](actions/get-river-stories.md) | GET | Retrieves stories from multiple feeds in NewsBlur. |
| [Get Stories By Hash](actions/get-stories-by-hash.md) | GET | Retrieves stories from NewsBlur by story hash. |
| [Mark Stories As Read](actions/mark-stories-as-read.md) | PUT | Marks stories as read in NewsBlur. |
| [Mark Story As Unread](actions/mark-story-as-unread.md) | PUT | Marks stories as unread in NewsBlur. |

### Story Text

| Action | Method | Description |
| --- | --- | --- |
| [Get Original Text](actions/get-original-text.md) | GET | Retrieves a story's original text from NewsBlur. |

### Unread Story Hash

| Action | Method | Description |
| --- | --- | --- |
| [List Unread Story Hashes](actions/list-unread-story-hashes.md) | GET | Retrieves unread story hashes from NewsBlur. |

