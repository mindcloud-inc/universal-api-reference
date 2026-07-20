# Enrich.so: Count Matching Leads

Retrieves lead counts from Enrich.so by search filters.

```
GET https://connect.mindcloud.co/v1/universal/enrich/latest/actions/count-matching-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Enrich.so `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/enrich/latest/actions/count-matching-leads?connectionId=$CONNECTION_ID&filters=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filters": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/enrich/latest/actions/count-matching-leads?${params}`, {
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
| `filters` | object | yes | Lead finder filter object. Default: `{"company":{"domains":["stripe.com"]}}`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `excludeFilters` | object | no | Optional filters to exclude. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of leads matching the filters. |
| `total` | number | Total matching lead count, when provided. |

## Native endpoint

Through the native Enrich.so API, this operation is `POST /lead-finder/count` (base URL `https://dev.enrich.so/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/count-matching-leads.md) for the provider-specific parameters and requirements.

