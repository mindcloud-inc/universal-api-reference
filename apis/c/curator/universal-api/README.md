# <img src="https://images.mindcloud.co/apps/icons/curator_1775845531445.png" alt="Curator logo" width="28" height="28"> Curator: Universal API

Manage Curator feeds, sources, posts, and custom posts through the Curator REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/curator/latest
- **Category:** Marketing / Social Media
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://curator.io
- **Vendor API docs:** https://curator.io/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Feeds](actions/list-feeds.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/curator/latest/actions/list-feeds?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Ads

| Action | Method | Description |
| --- | --- | --- |
| [Create Ad](actions/create-ad.md) | POST | Creates an ad or custom post in Curator. |
| [Delete Ad](actions/delete-ad.md) | DELETE | Deletes an existing ad or custom post from Curator. |
| [List Ads](actions/list-ads.md) | GET | Retrieves ads and custom posts from Curator. |
| [Update Ad](actions/update-ad.md) | PUT | Updates an existing ad or custom post in Curator. |

### Channels

| Action | Method | Description |
| --- | --- | --- |
| [Create Feed](actions/create-feed.md) | POST | Creates a feed in Curator. |
| [Delete Feed](actions/delete-feed.md) | DELETE | Deletes an existing feed from Curator. |
| [List Feeds](actions/list-feeds.md) | GET | Retrieves feeds from Curator. |
| [Update Feed](actions/update-feed.md) | PUT | Updates an existing feed in Curator. |

### Data Sources

| Action | Method | Description |
| --- | --- | --- |
| [Create Source](actions/create-source.md) | POST | Creates a source for a feed in Curator. |
| [Delete Source](actions/delete-source.md) | DELETE | Deletes an existing source from Curator. |
| [List Sources](actions/list-sources.md) | GET | Retrieves sources from Curator. |
| [Update Source](actions/update-source.md) | PUT | Updates an existing source in Curator. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [List Posts](actions/list-posts.md) | GET | Retrieves posts for a feed in Curator. |

