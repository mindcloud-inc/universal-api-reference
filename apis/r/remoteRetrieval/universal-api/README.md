# <img src="https://images.mindcloud.co/apps/icons/remote-retrieval_1775577531678.png" alt="Remote Retrieval logo" width="28" height="28"> Remote Retrieval: Universal API

Remote Retrieval helps IT, HR, and operations teams recover company-owned devices from remote employees through secure equipment-return logistics, order tracking, company details, and device-pricing APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/remoteRetrieval/latest
- **Category:** IT Operations / IT Service Management
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.remoteretrieval.com
- **Vendor API docs:** https://www.remoteretrieval.com/api-integration

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate User](actions/validate-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/remoteRetrieval/latest/actions/validate-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Details](actions/get-company-details.md) | GET | Retrieves company details from Remote Retrieval. |

### Device Price

| Action | Method | Description |
| --- | --- | --- |
| [Get Device Prices](actions/get-device-prices.md) | GET | Retrieves device prices from Remote Retrieval. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Validate User](actions/validate-user.md) | GET | Validates a user in Remote Retrieval. |

