# Stockpilot: Get Label Suggestion

Retrieves shipping label suggestions from Stockpilot.

```
GET https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/get-label-suggestion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stockpilot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/get-label-suggestion?connectionId=$CONNECTION_ID&orderPk=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderPk": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/get-label-suggestion?${params}`, {
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
| `orderPk` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "suggested": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `suggested` | object |  |

## Native endpoint

Through the native Stockpilot API, this operation is `GET /shipping/label-suggestion` (base URL `https://api.stockpilot.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-label-suggestion.md) for the provider-specific parameters and requirements.

