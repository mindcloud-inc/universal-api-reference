# <img src="https://images.mindcloud.co/apps/icons/nova-crm-logo_1783997323094.png" alt="Nova logo" width="28" height="28"> Nova: Universal API

Nova CRM and lead-operations API for authenticating tenant access, listing live lead lists, creating leads, and updating lead records.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nova/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://n0va.com
- **Vendor API docs:** https://app.n0va.com/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Authenticated Company](actions/get-authenticated-company.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nova/latest/actions/get-authenticated-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Authenticated Company](actions/get-authenticated-company.md) | GET |  |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Add Lead](actions/add-lead.md) | POST |  |
| [Update Lead](actions/update-lead.md) | PUT |  |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Get Live Lists](actions/get-live-lists.md) | GET |  |

