# Tiliter: Update Store

Updates a store in the Tiliter Recognition API.

```
PUT https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/update-store
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tiliter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/update-store" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "storeIdPath": "string",
  "storeId": "string",
  "region": "string",
  "friendlyName": "Ava Chen",
  "country": "string",
  "areaCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/update-store', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "storeIdPath": "string",
    "storeId": "string",
    "region": "string",
    "friendlyName": "Ava Chen",
    "country": "string",
    "areaCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `storeIdPath` | string | yes | Store ID in the request path. |
| `storeId` | string | yes | Store ID in the request body. Must match Store ID Path. |
| `region` | string | yes |  |
| `friendlyName` | string | yes |  |
| `country` | string | yes |  |
| `areaCode` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "areaCode": "string",
      "country": "string",
      "friendlyName": "Ava Chen",
      "region": "string",
      "storeId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `areaCode` | string |  |
| `country` | string |  |
| `friendlyName` | string |  |
| `region` | string |  |
| `storeId` | string |  |

## Native endpoint

Through the native Tiliter API, this operation is `PUT /stores/:store_id` (base URL `https://recognition.services.tiliter.com/v1/15`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-store.md) for the provider-specific parameters and requirements.

