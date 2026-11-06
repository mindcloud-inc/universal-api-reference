# <img src="https://images.mindcloud.co/apps/icons/swoogo_1791589994893.png" alt="Swoogo logo" width="28" height="28"> Swoogo: Universal API

Manage events, registrants, sessions, and attendance

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/swoogo/latest
- **Category:** Marketing / Events & Webinars
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://swoogo.events/
- **Vendor API docs:** https://swoogo.readme.io/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Events](actions/list-events.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swoogo/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Events](actions/list-events.md) | GET |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Update Registrant Contact ID](actions/update-registrant-contact-id.md) | PUT |  |

### Registrant

| Action | Method | Description |
| --- | --- | --- |
| [Get Registrant](actions/get-registrant.md) | GET |  |
| [List Registrants](actions/list-registrants.md) | GET |  |

