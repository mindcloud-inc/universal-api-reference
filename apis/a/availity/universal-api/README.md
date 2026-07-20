# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-04-21-as-13_1776789654312.png" alt="Availity logo" width="28" height="28"> Availity: Universal API

Availity provides REST APIs for HIPAA healthcare transactions, including payer lookup, eligibility and benefits, claim status, dental claims, and patient cost estimate workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/availity/latest
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.availity.com/
- **Vendor API docs:** https://developer.availity.com/blog/2025/3/25/hipaa-transactions

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Payers](actions/list-payers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/availity/latest/actions/list-payers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Claim Status

| Action | Method | Description |
| --- | --- | --- |
| [Create Claim Status Inquiry](actions/create-claim-status-inquiry.md) | POST | Creates a claim status inquiry in Availity. |
| [Delete Claim Status Inquiry](actions/delete-claim-status-inquiry.md) | DELETE | Deletes a claim status inquiry from Availity. |
| [Get Claim Status Inquiry](actions/get-claim-status-inquiry.md) | GET | Retrieves a claim status inquiry from Availity. |

### Coverage

| Action | Method | Description |
| --- | --- | --- |
| [Create Coverage Inquiry](actions/create-coverage-inquiry.md) | POST | Creates a coverage inquiry in Availity. |
| [Delete Coverage Inquiry](actions/delete-coverage-inquiry.md) | DELETE | Deletes a coverage inquiry from Availity. |
| [Get Coverage Inquiry](actions/get-coverage-inquiry.md) | GET | Retrieves a coverage inquiry from Availity. |

### Institutional Predetermination

| Action | Method | Description |
| --- | --- | --- |
| [Create Institutional Predetermination](actions/create-institutional-predetermination.md) | POST | Creates an institutional predetermination in Availity. |
| [Get Institutional Predetermination](actions/get-institutional-predetermination.md) | GET | Retrieves an institutional predetermination from Availity. |

### Payer

| Action | Method | Description |
| --- | --- | --- |
| [List Payers](actions/list-payers.md) | GET | Retrieves payers and supported transactions from Availity. |

### Professional Cost Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Create Professional Cost Estimate](actions/create-professional-cost-estimate.md) | POST | Creates a professional cost estimate in Availity. |
| [Get Professional Cost Estimate](actions/get-professional-cost-estimate.md) | GET | Retrieves a professional cost estimate from Availity. |

### Professional Predetermination

| Action | Method | Description |
| --- | --- | --- |
| [Create Professional Predetermination](actions/create-professional-predetermination.md) | POST | Creates a professional predetermination in Availity. |
| [Get Professional Predetermination](actions/get-professional-predetermination.md) | GET | Retrieves a professional predetermination from Availity. |

