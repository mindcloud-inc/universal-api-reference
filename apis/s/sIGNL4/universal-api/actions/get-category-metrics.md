# SIGNL4: Get Category Metrics

Retrieves category metrics from SIGNL4.

```
GET https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-category-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-category-metrics?connectionId=$CONNECTION_ID&teamId=string&categoryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string",
  "categoryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-category-metrics?${params}`, {
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
| `teamId` | string | yes | ID of the team the category belongs to |
| `categoryId` | string | yes | ID of the category to get |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categoryId": "string",
      "last24h": 1,
      "lastAlert": "2026-05-07T12:00:00.000Z",
      "subscriberCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryId` | string |  |
| `last24h` | number |  |
| `lastAlert` | date |  |
| `subscriberCount` | number |  |

## Native endpoint

Through the native SIGNL4 API, this operation is `GET /v2/categories/{teamId}/{categoryId}/metrics` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-category-metrics.md) for the provider-specific parameters and requirements.

