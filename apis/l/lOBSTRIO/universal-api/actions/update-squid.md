# LOBSTR.IO: Update Squid

Updates an existing squid in LOBSTR.IO.

```
PUT https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/update-squid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LOBSTR.IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/update-squid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "squidHash": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/update-squid', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "squidHash": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `isActive` | boolean | no | Enable (true) or disable (false) the squid. |
| `name` | string | no | Display name for the squid. |
| `squidHash` | string | yes | The unique identifier (hash) of the squid. |

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

Through the native LOBSTR.IO API, this operation is `POST /v1/squids/:squid_hash` (base URL `https://api.lobstr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-squid.md) for the provider-specific parameters and requirements.

