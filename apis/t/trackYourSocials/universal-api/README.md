# <img src="https://images.mindcloud.co/apps/icons/track-your-socials_1774389538101.png" alt="TrackYourSocials logo" width="28" height="28"> TrackYourSocials: Universal API

Unified social media analytics API that returns standardized engagement metrics and recent post data across major social platforms.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/trackYourSocials/latest
- **Category:** Marketing / Social Media
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://trackyoursocials.com
- **Vendor API docs:** https://trackyoursocials.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Post Analytics](actions/get-post-analytics.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackYourSocials/latest/actions/get-post-analytics?connectionId=$CONNECTION_ID&mediaLink=https%3A%2F%2Finstagram.com%2Fp%2FABC123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Social Post

| Action | Method | Description |
| --- | --- | --- |
| [Get Post Analytics](actions/get-post-analytics.md) | GET | Retrieves engagement metrics for a social media post from TrackYourSocials. |
| [List Last N Posts](actions/list-last-n-posts.md) | GET | Retrieves the last N posts from a social profile in TrackYourSocials. |
| [List Previous Day Posts](actions/list-previous-day-posts.md) | GET | Retrieves yesterday's posts from a social media channel in TrackYourSocials. |

