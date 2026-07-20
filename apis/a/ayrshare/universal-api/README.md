# <img src="https://images.mindcloud.co/apps/icons/favicon-www-ayrshare-com-48x48_1777038560356.png" alt="Ayrshare logo" width="28" height="28"> Ayrshare: Universal API

Unified social media API for publishing posts, managing post history, validating content, generating AI social copy, managing media, profiles, RSS feeds, webhooks, and retrieving social analytics across Ayrshare-supported networks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ayrshare/latest
- **Category:** Marketing
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ayrshare.com
- **Vendor API docs:** https://www.ayrshare.com/docs/apis/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Profile Details](actions/get-user-profile-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/get-user-profile-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Generate Profile JWT](actions/generate-profile-jwt.md) | POST | Generates a single sign-on JWT in Ayrshare. |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Add RSS Feed](actions/add-rss-feed.md) | POST | Creates a new RSS feed in Ayrshare. |
| [Check Post Length](actions/check-post-length.md) | GET | Checks post length against platform limits in Ayrshare. |
| [Delete Post](actions/delete-post.md) | DELETE | Deletes a post from Ayrshare. |
| [Delete RSS Feed](actions/delete-rss-feed.md) | DELETE | Deletes an RSS feed from Ayrshare. |
| [Get Post](actions/get-post.md) | GET | Retrieves a post by Ayrshare post ID. |
| [Get Post History By ID](actions/get-post-history-by-id.md) | GET | Retrieves post history by ID from Ayrshare. |
| [List Platform Post History](actions/list-platform-post-history.md) | GET | Retrieves post history for a platform from Ayrshare. |
| [List Post History](actions/list-post-history.md) | GET | Retrieves post history from Ayrshare. |
| [List RSS Feeds](actions/list-rss-feeds.md) | GET | Retrieves RSS feeds from Ayrshare. |
| [Moderate Content](actions/moderate-content.md) | GET | Checks text for harmful or inappropriate content in Ayrshare. |
| [Publish Post](actions/publish-post.md) | POST | Publishes a post to social networks with Ayrshare. |
| [Update RSS Feed](actions/update-rss-feed.md) | PUT | Updates an existing RSS feed in Ayrshare. |
| [Update Scheduled Post](actions/update-scheduled-post.md) | PUT | Updates a scheduled post in Ayrshare. |
| [Validate Post](actions/validate-post.md) | GET | Validates a post before publishing in Ayrshare. |

### Creative Assets

| Action | Method | Description |
| --- | --- | --- |
| [List Media Gallery](actions/list-media-gallery.md) | GET | Retrieves media from the Ayrshare gallery. |
| [Verify Media URL](actions/verify-media-url.md) | GET | Verifies a media URL in Ayrshare. |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Analyze Post Sentiment](actions/analyze-post-sentiment.md) | GET | Analyzes sentiment for a post or comment in Ayrshare. |
| [Generate Post Text](actions/generate-post-text.md) | POST | Generates a social post with AI in Ayrshare. |
| [Rewrite Post](actions/rewrite-post.md) | POST | Generates post rewrites with AI in Ayrshare. |
| [Translate Post](actions/translate-post.md) | POST | Translates a post in Ayrshare. |

### Landing Pages

| Action | Method | Description |
| --- | --- | --- |
| [Create Short Link](actions/create-short-link.md) | POST | Creates a short link in Ayrshare. |
| [Update Short Link](actions/update-short-link.md) | PUT | Updates a short link in Ayrshare. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Link Analytics](actions/get-link-analytics.md) | GET | Retrieves short link analytics from Ayrshare. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Check Banned Hashtag](actions/check-banned-hashtag.md) | GET | Checks whether a hashtag is banned in Ayrshare. |
| [Generate Auto Hashtags](actions/generate-auto-hashtags.md) | POST | Adds relevant hashtags to a post in Ayrshare. |
| [Recommend Hashtags](actions/recommend-hashtags.md) | GET | Finds hashtag suggestions by keyword in Ayrshare. |
| [Search Hashtags](actions/search-hashtags.md) | GET | Searches hashtag posts in Ayrshare. |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Create User Profile](actions/create-user-profile.md) | POST | Creates a new user profile in Ayrshare. |
| [List User Profiles](actions/list-user-profiles.md) | GET | Retrieves user profiles from Ayrshare. |
| [Update User Profile](actions/update-user-profile.md) | PUT | Updates an existing user profile in Ayrshare. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User Profile Details](actions/get-user-profile-details.md) | GET | Retrieves user profile details from Ayrshare. |

