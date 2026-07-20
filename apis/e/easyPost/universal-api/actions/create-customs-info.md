# EasyPost: Create Customs Info

Creates new customs info in EasyPost.

```
POST https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-customs-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-customs-info" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customsInfo": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-customs-info', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customsInfo": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customsInfo` | object | yes | CustomsInfo object to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentsType": "string",
      "customsCertify": true,
      "customsItems": [
        {}
      ],
      "customsSigner": "string",
      "eelPfc": "string",
      "id": "string",
      "mode": "string",
      "nonDeliveryOption": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentsType` | string |  |
| `customsCertify` | boolean |  |
| `customsItems` | array<object> |  |
| `customsSigner` | string |  |
| `eelPfc` | string |  |
| `id` | string |  |
| `mode` | string |  |
| `nonDeliveryOption` | string |  |
| `object` | string |  |

## Native endpoint

Through the native EasyPost API, this operation is `POST /customs_infos` (base URL `https://api.easypost.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customs-info.md) for the provider-specific parameters and requirements.

