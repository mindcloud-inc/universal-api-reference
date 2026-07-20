# Synchroteam: Initialize Quantities

Initializes part quantities in Synchroteam stock depots.

```
PUT https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/initialize-quantities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Synchroteam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/initialize-quantities" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "payload": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/initialize-quantities', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "payload": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `payload` | object | yes | Request body payload for updating inventory quantities (per docs). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "errors": [
        {
          "depot": "string",
          "parts": [
            {
              "quantity": 1,
              "reference": "string"
            }
          ]
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `errors[].depot` | string |  |
| `errors[].parts[].quantity` | number |  |
| `errors[].parts[].reference` | string |  |

## Native endpoint

Through the native Synchroteam API, this operation is `PUT /Api/v2/Inventory/Quantities` (base URL `https://ws.synchroteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/initialize-quantities.md) for the provider-specific parameters and requirements.

