# <img src="https://images.mindcloud.co/apps/icons/hacker-news-icon_1775745332900.png" alt="Hacker News logo" width="28" height="28"> Hacker News: Universal API

Read Hacker News stories, comments, users, and live update feeds from the public Hacker News API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hackerNews/latest
- **Actions:** 50
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://news.ycombinator.com/
- **Vendor API docs:** https://github.com/HackerNews/API

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Max Item ID](actions/get-max-item-id.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hackerNews/latest/actions/get-max-item-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (50)

### Ask Story

| Action | Method | Description |
| --- | --- | --- |
| [Get Ask Story](actions/get-ask-story.md) | GET | Retrieves an Ask HN story from Hacker News. |

### Ask Story Id

| Action | Method | Description |
| --- | --- | --- |
| [Get Ask Story ID By Rank](actions/get-ask-story-id-by-rank.md) | GET | Retrieves an Ask HN story ID from Hacker News by rank. |

### Ask Story Ids

| Action | Method | Description |
| --- | --- | --- |
| [Get Ask Story IDs](actions/get-ask-story-ids.md) | GET | Retrieves Ask HN story IDs from Hacker News. |

### Best Story Id

| Action | Method | Description |
| --- | --- | --- |
| [Get Best Story ID By Rank](actions/get-best-story-id-by-rank.md) | GET | Retrieves a best story ID from Hacker News by rank. |

### Best Story Ids

| Action | Method | Description |
| --- | --- | --- |
| [Get Best Story IDs](actions/get-best-story-ids.md) | GET | Retrieves best story IDs from Hacker News. |

### Child Item Id

| Action | Method | Description |
| --- | --- | --- |
| [Get Item Child ID By Index](actions/get-item-child-id-by-index.md) | GET | Retrieves an item child ID from Hacker News by index. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Get Comment](actions/get-comment.md) | GET | Retrieves a comment from Hacker News. |

### Item Author

| Action | Method | Description |
| --- | --- | --- |
| [Get Item Author](actions/get-item-author.md) | GET | Retrieves an item author from Hacker News. |

### Item Child Ids

| Action | Method | Description |
| --- | --- | --- |
| [Get Item Child IDs](actions/get-item-child-ids.md) | GET | Retrieves an item's child IDs from Hacker News. |

### Item Dead Flag

| Action | Method | Description |
| --- | --- | --- |
| [Get Item Dead Flag](actions/get-item-dead-flag.md) | GET | Retrieves an item dead flag from Hacker News. |

### Item Deleted Flag

| Action | Method | Description |
| --- | --- | --- |
| [Get Item Deleted Flag](actions/get-item-deleted-flag.md) | GET | Retrieves an item deleted flag from Hacker News. |

### Item Descendant Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Item Descendant Count](actions/get-item-descendant-count.md) | GET | Retrieves an item descendant count from Hacker News. |

### Item Id

| Action | Method | Description |
| --- | --- | --- |
| [Get Item ID](actions/get-item-id.md) | GET | Retrieves an item ID from Hacker News. |

### Item Score

| Action | Method | Description |
| --- | --- | --- |
| [Get Item Score](actions/get-item-score.md) | GET | Retrieves an item score from Hacker News. |

### Item Text

| Action | Method | Description |
| --- | --- | --- |
| [Get Item Text](actions/get-item-text.md) | GET | Retrieves an item text body from Hacker News. |

### Item Time

| Action | Method | Description |
| --- | --- | --- |
| [Get Item Time](actions/get-item-time.md) | GET | Retrieves an item timestamp from Hacker News. |

### Item Title

| Action | Method | Description |
| --- | --- | --- |
| [Get Item Title](actions/get-item-title.md) | GET | Retrieves an item title from Hacker News. |

### Item Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Item Type](actions/get-item-type.md) | GET | Retrieves an item type from Hacker News. |

### Item Url

| Action | Method | Description |
| --- | --- | --- |
| [Get Item URL](actions/get-item-url.md) | GET | Retrieves an item URL from Hacker News. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Get Item](actions/get-item.md) | GET | Retrieves an item from Hacker News. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Job](actions/get-job.md) | GET | Retrieves a job post from Hacker News. |

### Job Story Id

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Story ID By Rank](actions/get-job-story-id-by-rank.md) | GET | Retrieves a job story ID from Hacker News by rank. |

### Job Story Ids

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Story IDs](actions/get-job-story-ids.md) | GET | Retrieves job story IDs from Hacker News. |

### Max Item Id

| Action | Method | Description |
| --- | --- | --- |
| [Get Max Item ID](actions/get-max-item-id.md) | GET | Retrieves the maximum item ID from Hacker News. |

### New Story Id

| Action | Method | Description |
| --- | --- | --- |
| [Get New Story ID By Rank](actions/get-new-story-id-by-rank.md) | GET | Retrieves a new story ID from Hacker News by rank. |

### New Story Ids

| Action | Method | Description |
| --- | --- | --- |
| [Get New Story IDs](actions/get-new-story-ids.md) | GET | Retrieves new story IDs from Hacker News. |

### Parent Item Id

| Action | Method | Description |
| --- | --- | --- |
| [Get Item Parent](actions/get-item-parent.md) | GET | Retrieves an item parent ID from Hacker News. |

### Poll

| Action | Method | Description |
| --- | --- | --- |
| [Get Poll](actions/get-poll.md) | GET | Retrieves a poll from Hacker News. |

### Poll Id

| Action | Method | Description |
| --- | --- | --- |
| [Get Item Poll ID](actions/get-item-poll-id.md) | GET | Retrieves an item poll ID from Hacker News. |

### Poll Option

| Action | Method | Description |
| --- | --- | --- |
| [Get Poll Option](actions/get-poll-option.md) | GET | Retrieves a poll option from Hacker News. |

### Poll Option Id

| Action | Method | Description |
| --- | --- | --- |
| [Get Poll Option ID By Index](actions/get-poll-option-id-by-index.md) | GET | Retrieves a poll option ID from Hacker News by index. |

### Poll Option Ids

| Action | Method | Description |
| --- | --- | --- |
| [Get Poll Option IDs](actions/get-poll-option-ids.md) | GET | Retrieves a poll's option IDs from Hacker News. |

### Show Story

| Action | Method | Description |
| --- | --- | --- |
| [Get Show Story](actions/get-show-story.md) | GET | Retrieves a Show HN story from Hacker News. |

### Show Story Id

| Action | Method | Description |
| --- | --- | --- |
| [Get Show Story ID By Rank](actions/get-show-story-id-by-rank.md) | GET | Retrieves a Show HN story ID from Hacker News by rank. |

### Show Story Ids

| Action | Method | Description |
| --- | --- | --- |
| [Get Show Story IDs](actions/get-show-story-ids.md) | GET | Retrieves Show HN story IDs from Hacker News. |

### Story

| Action | Method | Description |
| --- | --- | --- |
| [Get Story](actions/get-story.md) | GET | Retrieves a story from Hacker News. |

### Top Story Id

| Action | Method | Description |
| --- | --- | --- |
| [Get Top Story ID By Rank](actions/get-top-story-id-by-rank.md) | GET | Retrieves a top story ID from Hacker News by rank. |

### Top Story Ids

| Action | Method | Description |
| --- | --- | --- |
| [Get Top Story IDs](actions/get-top-story-ids.md) | GET | Retrieves top story IDs from Hacker News. |

### Update Feed

| Action | Method | Description |
| --- | --- | --- |
| [Get Updates](actions/get-updates.md) | GET | Retrieves item and profile updates from Hacker News. |

### Updated Item Id

| Action | Method | Description |
| --- | --- | --- |
| [Get Updated Item ID By Index](actions/get-updated-item-id-by-index.md) | GET | Retrieves an updated item ID from Hacker News by index. |

### Updated Item Ids

| Action | Method | Description |
| --- | --- | --- |
| [Get Updated Item IDs](actions/get-updated-item-ids.md) | GET | Retrieves updated item IDs from Hacker News. |

### Updated Profile Id

| Action | Method | Description |
| --- | --- | --- |
| [Get Updated Profile ID By Index](actions/get-updated-profile-id-by-index.md) | GET | Retrieves an updated profile ID from Hacker News by index. |

### Updated Profile Ids

| Action | Method | Description |
| --- | --- | --- |
| [Get Updated Profile IDs](actions/get-updated-profile-ids.md) | GET | Retrieves updated profile IDs from Hacker News. |

### User About

| Action | Method | Description |
| --- | --- | --- |
| [Get User About](actions/get-user-about.md) | GET | Retrieves a user's about text from Hacker News. |

### User Created

| Action | Method | Description |
| --- | --- | --- |
| [Get User Created](actions/get-user-created.md) | GET | Retrieves a user's creation time from Hacker News. |

### User Id

| Action | Method | Description |
| --- | --- | --- |
| [Get User ID](actions/get-user-id.md) | GET | Retrieves a user ID from Hacker News. |

### User Karma

| Action | Method | Description |
| --- | --- | --- |
| [Get User Karma](actions/get-user-karma.md) | GET | Retrieves a user's karma from Hacker News. |

### User Submission Id

| Action | Method | Description |
| --- | --- | --- |
| [Get User Submission ID By Index](actions/get-user-submission-id-by-index.md) | GET | Retrieves a user submission ID from Hacker News by index. |

### User Submission Ids

| Action | Method | Description |
| --- | --- | --- |
| [Get User Submission IDs](actions/get-user-submission-ids.md) | GET | Retrieves a user's submission IDs from Hacker News. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Hacker News. |

