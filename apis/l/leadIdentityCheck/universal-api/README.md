# <img src="https://images.mindcloud.co/apps/icons/lead-identity-check-icon_1775679093271.png" alt="Lead Identity Check logo" width="28" height="28"> Lead Identity Check: Universal API

Verify lead identity using Lead Identity Check filters and lead scoring signals across phone, email, and address inputs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/leadIdentityCheck/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://leadidentitycheck.com
- **Vendor API docs:** https://leadidentitycheck.com/documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Authenticate Connection](actions/authenticate-connection.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadIdentityCheck/latest/actions/authenticate-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [List Filter Categories](actions/list-filter-categories.md) | GET |  |

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [Verify Lead](actions/verify-lead.md) | GET |  |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Authenticate Connection](actions/authenticate-connection.md) | GET |  |

