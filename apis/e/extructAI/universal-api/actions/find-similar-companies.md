# Extruct AI: Find Similar Companies

Finds similar companies in Extruct AI.

```
GET https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/find-similar-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extruct AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/find-similar-companies?connectionId=$CONNECTION_ID&limit=25&offset=0&company_identifier=trustpayments.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "company_identifier": "trustpayments.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/find-similar-companies?${params}`, {
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
| `company_identifier` | string | yes | Reference company UUID or domain. Example: `trustpayments.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filters` | string | no | JSON string of SearchFilters. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "facetCounts": [
        {}
      ],
      "referenceCompany": {},
      "request": {},
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `facetCounts` | array<object> |  |
| `referenceCompany` | object |  |
| `request` | object |  |
| `results` | array<object> |  |

## Native endpoint

Through the native Extruct AI API, this operation is `GET /v1/companies/:company_identifier/similar` (base URL `https://api.extruct.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/find-similar-companies.md) for the provider-specific parameters and requirements.

