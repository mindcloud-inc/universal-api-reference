# Stockpilot: Retrieve Shipping Label

Retrieves a shipping label from Stockpilot.

```
GET https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/retrieve-shipping-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stockpilot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/retrieve-shipping-label?connectionId=$CONNECTION_ID&entityId=string&service=string&orderPk=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entityId": "string",
  "service": "string",
  "orderPk": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/retrieve-shipping-label?${params}`, {
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
| `service` | string | yes |  |
| `orderPk` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        [
          1
        ]
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | array<number> |  |
| `type` | string |  |

## Native endpoint

Through the native Stockpilot API, this operation is `POST /shipping/retrieve-label` (base URL `https://api.stockpilot.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-shipping-label.md) for the provider-specific parameters and requirements.

