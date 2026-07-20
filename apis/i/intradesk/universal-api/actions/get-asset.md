# Intradesk: Get Asset

Retrieves an asset from Intradesk.

```
GET https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/get-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intradesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/get-asset?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/get-asset?${params}`, {
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
| `id` | string | yes | Asset identifier from Intradesk Settings API path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assetAddress": {},
      "assetAddressId": 1,
      "client": {},
      "clientId": 1,
      "description": "string",
      "id": 1,
      "inventoryNumber": "string",
      "isArchived": true,
      "isNameStartsFromInventory": true,
      "name": "Ava Chen",
      "nameManually": "Ava Chen",
      "ownerId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assetAddress` | object |  |
| `assetAddressId` | number |  |
| `client` | object |  |
| `clientId` | number |  |
| `description` | string |  |
| `id` | number |  |
| `inventoryNumber` | string |  |
| `isArchived` | boolean |  |
| `isNameStartsFromInventory` | boolean |  |
| `name` | string |  |
| `nameManually` | string |  |
| `ownerId` | number |  |

## Native endpoint

Through the native Intradesk API, this operation is `GET /settings/api/v1/Assets/{id}` (base URL `https://apigw.intradesk.ru`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asset.md) for the provider-specific parameters and requirements.

