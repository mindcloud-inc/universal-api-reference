# Curator: Create Source

Creates a source for a feed in Curator.

```
POST https://connect.mindcloud.co/v1/universal/curator/latest/actions/create-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Curator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/curator/latest/actions/create-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "feedId": "string",
  "sourceType": 1,
  "tag": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/curator/latest/actions/create-source', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "feedId": "string",
    "sourceType": 1,
    "tag": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `feedId` | string | yes | Feed to assign the source to. |
| `sourceType` | number | yes | Curator source type ID. |
| `tag` | string | yes | Source tag or lookup value. |

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

Through the native Curator API, this operation is `POST /v1/sources` (base URL `https://api.curator.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-source.md) for the provider-specific parameters and requirements.

