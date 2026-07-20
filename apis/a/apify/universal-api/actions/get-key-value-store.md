# Apify: Get Key-Value Store

Retrieves a key-value store from Apify.

```
GET https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-key-value-store
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-key-value-store?connectionId=$CONNECTION_ID&storeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "storeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-key-value-store?${params}`, {
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
| `storeId` | string | yes | The ID of the key-value store to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "accessedAt": "2026-05-07T12:00:00.000Z",
        "actId": {},
        "actRunId": {},
        "consoleUrl": "https://example.com",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "generalAccess": "string",
        "id": "string",
        "keysPublicUrl": "https://example.com",
        "modifiedAt": "2026-05-07T12:00:00.000Z",
        "name": "Ava Chen",
        "recordsPublicUrl": "https://example.com",
        "schema": {},
        "stats": {
          "deleteCount": 1,
          "listCount": 1,
          "readCount": 1,
          "storageBytes": 1,
          "writeCount": 1
        },
        "urlSigningSecretKey": "https://example.com",
        "userId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.accessedAt` | date |  |
| `data.actId` | object |  |
| `data.actRunId` | object |  |
| `data.consoleUrl` | string |  |
| `data.createdAt` | date |  |
| `data.generalAccess` | string |  |
| `data.id` | string |  |
| `data.keysPublicUrl` | string |  |
| `data.modifiedAt` | date |  |
| `data.name` | string |  |
| `data.recordsPublicUrl` | string |  |
| `data.schema` | object |  |
| `data.stats.deleteCount` | number |  |
| `data.stats.listCount` | number |  |
| `data.stats.readCount` | number |  |
| `data.stats.storageBytes` | number |  |
| `data.stats.writeCount` | number |  |
| `data.urlSigningSecretKey` | string |  |
| `data.userId` | string |  |

## Native endpoint

Through the native Apify API, this operation is `GET /v2/key-value-stores/:storeId` (base URL `https://api.apify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-key-value-store.md) for the provider-specific parameters and requirements.

