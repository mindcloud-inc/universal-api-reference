# <img src="https://images.mindcloud.co/apps/icons/just-sift-icon_1776796080342.png" alt="JustSift logo" width="28" height="28"> JustSift: Universal API

Access Sift people directory profiles, search, media, and field metadata through the official JustSift API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/justSift/latest
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.justsift.com
- **Vendor API docs:** https://developers.justsift.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Person Fields](actions/list-person-fields.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/justSift/latest/actions/list-person-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Field

| Action | Method | Description |
| --- | --- | --- |
| [List Person Fields](actions/list-person-fields.md) | GET |  |

### Media

| Action | Method | Description |
| --- | --- | --- |
| [Get Person Media](actions/get-person-media.md) | GET |  |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Advanced People Search](actions/advanced-people-search.md) | GET |  |
| [Get Person](actions/get-person.md) | GET |  |
| [Search People](actions/search-people.md) | GET |  |

