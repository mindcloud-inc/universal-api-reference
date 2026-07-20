# Syntage: Get Sales Revenue Insight

Retrieves sales revenue insight for an entity in Syntage.

```
GET https://connect.mindcloud.co/v1/universal/syntage/latest/actions/get-sales-revenue-insight
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syntage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syntage/latest/actions/get-sales-revenue-insight?connectionId=$CONNECTION_ID&entityId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entityId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syntage/latest/actions/get-sales-revenue-insight?${params}`, {
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
| `entityId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "stats": [
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
| `data` | array<object> |  |
| `stats` | array<object> |  |

## Native endpoint

Through the native Syntage API, this operation is `GET /entities/:entityId/insights/sales-revenue` (base URL `https://api.sandbox.syntage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sales-revenue-insight.md) for the provider-specific parameters and requirements.

