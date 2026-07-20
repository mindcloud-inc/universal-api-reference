# Starshipit: Print Labels



```
POST https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/print-labels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starshipit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/print-labels" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/print-labels', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderIds[]` | array<number> | no |  |
| `reprint` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "labels": [
        {
          "labelBase64String": "string",
          "labelType": "string"
        }
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `labels` | array<object> |  |
| `labels[].labelBase64String` | string |  |
| `labels[].labelType` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Starshipit API, this operation is `POST /orders/shipments` (base URL `https://api.starshipit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/print-labels.md) for the provider-specific parameters and requirements.

