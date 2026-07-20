# Tiliter: Get Store

Retrieves a store from the Tiliter Recognition API.

```
GET https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/get-store
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tiliter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/get-store?connectionId=$CONNECTION_ID&storeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "storeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/get-store?${params}`, {
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
| `storeId` | string | yes |  |

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

Through the native Tiliter API, this operation is `GET /stores/:store_id` (base URL `https://recognition.services.tiliter.com/v1/15`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-store.md) for the provider-specific parameters and requirements.

