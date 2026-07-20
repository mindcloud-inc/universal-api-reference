# <img src="https://images.mindcloud.co/apps/icons/favicon-support-myownconference-com-48x48_1776802902140.png" alt="MyOwnConference logo" width="28" height="28"> MyOwnConference: Universal API

MyOwnConference is a webinar platform for scheduling webinars, managing attendees and moderators, and controlling webinar automation through the MyOwnConference public API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/myOwnConference/latest
- **Category:** Marketing
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://myownconference.com
- **Vendor API docs:** https://support.myownconference.com/en/article/myownconference-public-api-o6or9a/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get profile](actions/get-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myOwnConference/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Events

| Action | Method | Description |
| --- | --- | --- |
| [List webinars](actions/list-webinars.md) | GET | Retrieves scheduled webinars from MyOwnConference. |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Get profile](actions/get-profile.md) | GET | Retrieves the current MyOwnConference account profile. |

