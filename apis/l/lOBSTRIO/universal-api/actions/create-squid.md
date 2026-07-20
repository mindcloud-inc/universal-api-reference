# LOBSTR.IO: Create Squid

Creates a new squid in LOBSTR.IO.

```
POST https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/create-squid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LOBSTR.IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/create-squid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "crawler": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/create-squid', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "crawler": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `crawler` | string | yes | The unique ID (hash) of the crawler to use for this squid. |
| `name` | string | no | Custom name for the squid. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": [
        {}
      ],
      "concurrency": 1,
      "crawler": "string",
      "createdAt": "string",
      "id": "string",
      "isActive": true,
      "name": "Ava Chen",
      "params": {},
      "schedule": {},
      "toComplete": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | array<object> |  |
| `concurrency` | number |  |
| `crawler` | string |  |
| `createdAt` | string |  |
| `id` | string |  |
| `isActive` | boolean |  |
| `name` | string |  |
| `params` | object |  |
| `schedule` | object |  |
| `toComplete` | boolean |  |

## Native endpoint

Through the native LOBSTR.IO API, this operation is `POST /v1/squids` (base URL `https://api.lobstr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-squid.md) for the provider-specific parameters and requirements.

