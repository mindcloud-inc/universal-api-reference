# Samsara: List Trailers



```
GET https://connect.mindcloud.co/v1/universal/samsara/latest/actions/list-trailers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Samsara `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/samsara/latest/actions/list-trailers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/samsara/latest/actions/list-trailers?${params}`, {
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
      "enabledForMobile": true,
      "externalIds": {
        "samsara": {
          "serial": "string",
          "vin": "string"
        }
      },
      "id": "string",
      "installedGateway": {
        "model": "string",
        "serial": "string"
      },
      "name": "Ava Chen",
      "tags": [
        {
          "id": "string",
          "name": "Ava Chen"
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
| `enabledForMobile` | boolean |  |
| `externalIds.samsara.serial` | string |  |
| `externalIds.samsara.vin` | string |  |
| `id` | string |  |
| `installedGateway.model` | string |  |
| `installedGateway.serial` | string |  |
| `name` | string |  |
| `tags[].id` | string |  |
| `tags[].name` | string |  |

## Native endpoint

Through the native Samsara API, this operation is `GET fleet/trailers` (base URL `https://api.samsara.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-trailers.md) for the provider-specific parameters and requirements.

