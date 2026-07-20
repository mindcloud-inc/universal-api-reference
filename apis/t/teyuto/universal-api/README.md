# <img src="https://images.mindcloud.co/apps/icons/apple-icon-180x180_1775165146626.png" alt="Teyuto logo" width="28" height="28"> Teyuto: Universal API

Manage channels, videos, live streams, and OTT content on Teyuto's video platform.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/teyuto/latest
- **Category:** Communication / Video Communications
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://teyuto.com/
- **Vendor API docs:** https://apidocs.teyuto.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teyuto/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Channels

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel Settings](actions/get-channel-settings.md) | GET | Retrieves current channel settings from Teyuto. |

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [Get Collection](actions/get-collection.md) | GET | Retrieves a specific collection from Teyuto. |
| [List Collections](actions/list-collections.md) | GET | Retrieves all collections from a Teyuto channel. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Delete Session](actions/delete-session.md) | DELETE | Deletes an existing authenticated Teyuto session. |
| [Generate Session](actions/generate-session.md) | POST | Creates an authenticated session in Teyuto. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in Teyuto. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes an existing tag from Teyuto. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a specific tag from Teyuto. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in Teyuto. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Collections Analytics](actions/get-collections-analytics.md) | GET | Retrieves collection analytics from a Teyuto channel. |
| [Get General Analytics](actions/get-general-analytics.md) | GET | Retrieves general analytics from a Teyuto channel. |
| [Get Video](actions/get-video.md) | GET | Retrieves a specific video from Teyuto. |
| [Get Videos Analytics](actions/get-videos-analytics.md) | GET | Retrieves video analytics from a Teyuto channel. |
| [List Packages](actions/list-packages.md) | GET | Retrieves all packages from a Teyuto channel. |
| [List Restreams](actions/list-restreams.md) | GET | Retrieves all restreams from a Teyuto channel. |
| [List Videos](actions/list-videos.md) | GET | Retrieves all videos from a Teyuto channel. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in Teyuto. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes an existing user from Teyuto. |
| [List Users](actions/list-users.md) | GET | Retrieves all users from a Teyuto account. |

