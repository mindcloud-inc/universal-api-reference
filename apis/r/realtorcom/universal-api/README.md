# <img src="https://images.mindcloud.co/apps/icons/realtor-dot-com-icon_1777931014562.png" alt="Realtor.com logo" width="28" height="28"> Realtor.com: Universal API

Access Realtor.com/Move ListHub publisher listing data through the official ListHub Syndication API for property import, listing lookup, metadata, and sync workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/realtorcom/latest
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.realtor.com/
- **Vendor API docs:** https://www.listhub.com/api-documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Properties](actions/list-properties.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/realtorcom/latest/actions/list-properties?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Metadata](actions/get-metadata.md) | GET |  |

### Property

| Action | Method | Description |
| --- | --- | --- |
| [Get Property](actions/get-property.md) | GET |  |
| [List Properties](actions/list-properties.md) | GET |  |

### Property Sync

| Action | Method | Description |
| --- | --- | --- |
| [Sync Properties](actions/sync-properties.md) | GET |  |

