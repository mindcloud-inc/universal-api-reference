# LOBSTR.IO: Get Squid Details

Retrieves squid details from LOBSTR.IO.

```
GET https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/get-squid-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LOBSTR.IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/get-squid-details?connectionId=$CONNECTION_ID&squidHash=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "squidHash": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/get-squid-details?${params}`, {
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
| `squidHash` | string | yes | The unique identifier (hash) of the squid. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "concurrency": 1,
      "crawler": "string",
      "crawlerName": "Ava Chen",
      "createdAt": "string",
      "icon": "string",
      "id": "string",
      "isActive": true,
      "isReady": true,
      "message": "string",
      "name": "Ava Chen",
      "params": {},
      "toComplete": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `concurrency` | number |  |
| `crawler` | string |  |
| `crawlerName` | string |  |
| `createdAt` | string |  |
| `icon` | string |  |
| `id` | string |  |
| `isActive` | boolean |  |
| `isReady` | boolean |  |
| `message` | string |  |
| `name` | string |  |
| `params` | object |  |
| `toComplete` | boolean |  |

## Native endpoint

Through the native LOBSTR.IO API, this operation is `GET /v1/squids/:squid_hash` (base URL `https://api.lobstr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-squid-details.md) for the provider-specific parameters and requirements.

