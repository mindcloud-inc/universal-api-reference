# Prospeo: Bulk Enrich Companies

Retrieves enriched company data from Prospeo in bulk.

```
GET https://connect.mindcloud.co/v1/universal/prospeo/latest/actions/bulk-enrich-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prospeo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prospeo/latest/actions/bulk-enrich-companies?connectionId=$CONNECTION_ID&data%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "data[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prospeo/latest/actions/bulk-enrich-companies?${params}`, {
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
| `data[]` | array<object> | yes | Company records to enrich, up to 50 at once. Default: `[{"identifier":"microsoft","company_website":"microsoft.com"}]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "invalidDatapoints": [
        {}
      ],
      "matched": [
        {}
      ],
      "notMatched": [
        {}
      ],
      "totalCost": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `invalidDatapoints` | array<object> |  |
| `matched` | array<object> |  |
| `notMatched` | array<object> |  |
| `totalCost` | number |  |

## Native endpoint

Through the native Prospeo API, this operation is `POST /bulk-enrich-company` (base URL `https://api.prospeo.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-enrich-companies.md) for the provider-specific parameters and requirements.

