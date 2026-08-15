# Samsara: List Assets



```
GET https://connect.mindcloud.co/v1/universal/samsara/latest/actions/list-assets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Samsara `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/samsara/latest/actions/list-assets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/samsara/latest/actions/list-assets?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAtTime": "string",
      "id": "string",
      "licensePlate": "string",
      "make": "string",
      "model": "string",
      "name": "Ava Chen",
      "readingsIngestionEnabled": true,
      "regulationMode": "string",
      "type": "string",
      "updatedAtTime": "string",
      "vin": "string",
      "year": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAtTime` | string |  |
| `id` | string |  |
| `licensePlate` | string |  |
| `make` | string |  |
| `model` | string |  |
| `name` | string |  |
| `readingsIngestionEnabled` | boolean |  |
| `regulationMode` | string |  |
| `type` | string |  |
| `updatedAtTime` | string |  |
| `vin` | string |  |
| `year` | number |  |

## Native endpoint

Through the native Samsara API, this operation is `GET assets` (base URL `https://api.samsara.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-assets.md) for the provider-specific parameters and requirements.

