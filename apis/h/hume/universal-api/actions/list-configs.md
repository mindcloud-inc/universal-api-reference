# Hume: List configs



```
GET https://connect.mindcloud.co/v1/universal/hume/latest/actions/list-configs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hume `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hume/latest/actions/list-configs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hume/latest/actions/list-configs?${params}`, {
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
      "createdOn": 1,
      "eviVersion": "string",
      "id": "string",
      "languageModel": {},
      "modifiedOn": 1,
      "name": "Ava Chen",
      "prompt": {},
      "version": 1,
      "versionType": "string",
      "voice": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdOn` | number |  |
| `eviVersion` | string |  |
| `id` | string |  |
| `languageModel` | object |  |
| `modifiedOn` | number |  |
| `name` | string |  |
| `prompt` | object |  |
| `version` | number |  |
| `versionType` | string |  |
| `voice` | object |  |

## Native endpoint

Through the native Hume API, this operation is `GET /v0/evi/configs` (base URL `https://api.hume.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-configs.md) for the provider-specific parameters and requirements.

