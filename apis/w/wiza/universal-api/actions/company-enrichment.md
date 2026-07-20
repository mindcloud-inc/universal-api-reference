# Wiza: Company Enrichment

Retrieves enriched company data from Wiza.

```
GET https://connect.mindcloud.co/v1/universal/wiza/latest/actions/company-enrichment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wiza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wiza/latest/actions/company-enrichment?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wiza/latest/actions/company-enrichment?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `company_name` | string | no | Company name to enrich. |
| `company_domain` | string | no | Company domain to enrich. |
| `company_linkedin_id` | string | no | LinkedIn company ID to enrich. |
| `company_linkedin_slug` | string | no | LinkedIn company slug to enrich. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "company_domain": "string",
        "company_industry": "string",
        "company_linkedin": "https://example.com",
        "company_location": "string",
        "company_name": "Ava Chen",
        "company_size": 1,
        "credits": {
          "api_credits": {
            "total": 1
          }
        }
      },
      "status": {
        "code": 1,
        "message": "string"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.company_domain` | string | Company domain. |
| `data.company_industry` | string | Company industry. |
| `data.company_linkedin` | string | Company LinkedIn URL. |
| `data.company_location` | string | Company location. |
| `data.company_name` | string | Company name. |
| `data.company_size` | number | Company size. |
| `data.credits.api_credits.total` | number | API credits charged for the enrichment. |
| `status.code` | number | HTTP-style status code returned by Wiza. |
| `status.message` | string | Status message from Wiza. |
| `type` | string | Response type identifier. |

## Native endpoint

Through the native Wiza API, this operation is `POST /company_enrichments` (base URL `https://wiza.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/company-enrichment.md) for the provider-specific parameters and requirements.

