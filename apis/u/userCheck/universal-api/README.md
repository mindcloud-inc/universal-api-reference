# <img src="https://images.mindcloud.co/apps/icons/user-check_1774882390177.png" alt="UserCheck logo" width="28" height="28"> UserCheck: Universal API

Validate emails, inspect domains, and manage domain blocklists

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/userCheck/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.usercheck.com
- **Vendor API docs:** https://www.usercheck.com/docs/api/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Status](actions/get-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userCheck/latest/actions/get-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Blocklist Entry

| Action | Method | Description |
| --- | --- | --- |
| [Add Domain to Blocklist](actions/add-domain-to-blocklist.md) | POST | Adds a domain to the UserCheck blocklist. |
| [Bulk Add Domains to Blocklist](actions/bulk-add-domains-to-blocklist.md) | POST | Adds multiple domains to the UserCheck blocklist. |
| [Get Blocklisted Domain](actions/get-blocklisted-domain.md) | GET | Retrieves a blocklisted domain from UserCheck. |
| [List Blocklisted Domains](actions/list-blocklisted-domains.md) | GET | Retrieves blocklisted domain entries from UserCheck. |
| [Remove Domain from Blocklist](actions/remove-domain-from-blocklist.md) | DELETE | Removes a domain from the UserCheck blocklist. |

### Domain Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate Domain](actions/validate-domain.md) | GET | Retrieves domain validation details from UserCheck. |

### Email Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate Email](actions/validate-email.md) | GET | Retrieves email validation details from UserCheck. |

### Gate Decision

| Action | Method | Description |
| --- | --- | --- |
| [Evaluate Gate Decision](actions/evaluate-gate-decision.md) | POST | Requests a gate decision from UserCheck. |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Status](actions/get-status.md) | GET | Retrieves account status details from UserCheck. |

