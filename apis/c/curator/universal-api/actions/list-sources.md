# Curator: List Sources

Retrieves sources from Curator.

```
GET https://connect.mindcloud.co/v1/universal/curator/latest/actions/list-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Curator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/curator/latest/actions/list-sources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/curator/latest/actions/list-sources?${params}`, {
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
| `feedId` | string | no | Optional feed filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "defaultUserImage": "string",
      "errorCount": 1,
      "feedId": "string",
      "id": "string",
      "interval": 1,
      "name": "Ava Chen",
      "networkId": 1,
      "postCount": 1,
      "response": {},
      "sourceType": {},
      "status": "string",
      "tag": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `defaultUserImage` | string |  |
| `errorCount` | number |  |
| `feedId` | string |  |
| `id` | string |  |
| `interval` | number |  |
| `name` | string |  |
| `networkId` | number |  |
| `postCount` | number |  |
| `response` | object |  |
| `sourceType` | object |  |
| `status` | string |  |
| `tag` | string |  |

## Native endpoint

Through the native Curator API, this operation is `GET /v1/sources` (base URL `https://api.curator.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sources.md) for the provider-specific parameters and requirements.

