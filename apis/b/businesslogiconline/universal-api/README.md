# <img src="https://images.mindcloud.co/apps/icons/businesslogic-icon_1776087048466.png" alt="Businesslogic.online logo" width="28" height="28"> Businesslogic.online: Universal API

Access Businesslogic.online calculator metadata and execute calculator inputs through the public describe and execute API endpoints.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/businesslogiconline/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.businesslogic.online
- **Vendor API docs:** https://api.businesslogic.online/describe

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Describe Calculator](actions/describe-calculator.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/businesslogiconline/latest/actions/describe-calculator?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Calculator

| Action | Method | Description |
| --- | --- | --- |
| [Describe Calculator](actions/describe-calculator.md) | GET | Retrieves calculator input and output schemas from Businesslogic.online. |

### Calculator Execution

| Action | Method | Description |
| --- | --- | --- |
| [Execute Calculator](actions/execute-calculator.md) | POST | Executes a calculator with input values in Businesslogic.online. |

