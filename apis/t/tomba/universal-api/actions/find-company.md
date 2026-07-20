# Tomba: Find Company

Retrieves company enrichment data from Tomba.

```
GET https://connect.mindcloud.co/v1/universal/tomba/latest/actions/find-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tomba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tomba/latest/actions/find-company?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tomba/latest/actions/find-company?${params}`, {
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
| `domain` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "domain": "string",
      "emailProvider": "ava@example.com",
      "geo": {
        "city": "string",
        "countryCode": "string"
      },
      "indexedAt": "2026-05-07T12:00:00.000Z",
      "legalName": "Ava Chen",
      "linkedin": {
        "handle": "https://example.com"
      },
      "metrics": {
        "employees": "string"
      },
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `domain` | string |  |
| `emailProvider` | string |  |
| `geo.city` | string |  |
| `geo.countryCode` | string |  |
| `indexedAt` | date |  |
| `legalName` | string |  |
| `linkedin.handle` | string |  |
| `metrics.employees` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Tomba API, this operation is `GET /companies/find` (base URL `https://api.tomba.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-company.md) for the provider-specific parameters and requirements.

