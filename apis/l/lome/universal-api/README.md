# <img src="https://images.mindcloud.co/apps/icons/lome_1774903006907.png" alt="Lome logo" width="28" height="28"> Lome: Universal API

Create event sign ups, track responses, and manage contacts

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lome/latest
- **Category:** Marketing / Events & Webinars
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.withlome.com
- **Vendor API docs:** https://grow.withlome.com/articles/lome/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Communities](actions/list-communities.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lome/latest/actions/list-communities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Community

| Action | Method | Description |
| --- | --- | --- |
| [List Communities](actions/list-communities.md) | GET | Retrieves your hosted communities from Lome. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Lome. |

### Response

| Action | Method | Description |
| --- | --- | --- |
| [List Recent Community Responses](actions/list-recent-community-responses.md) | GET | Retrieves recent responses for a specific Lome community. |
| [List Recent Responses](actions/list-recent-responses.md) | GET | Retrieves sign up form responses from the last 24 hours in Lome. |

