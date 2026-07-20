# NetExplorer: Get Received



```
GET https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-signatures-received
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-signatures-received?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-signatures-received?${params}`, {
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
      "nbObjects": 1,
      "nbTotalObjects": 1,
      "objects": [
        {
          "askedAt": "2026-05-07T12:00:00.000Z",
          "askedBy": "string",
          "email": "ava@example.com",
          "firstName": "Ava",
          "id": "string",
          "lastName": "Chen",
          "link": "https://example.com",
          "phone": "string",
          "position": 1,
          "refuseAt": "string",
          "refuseReason": "string",
          "signatureId": 1,
          "signatureName": "Ava Chen",
          "status": "string",
          "type": "string",
          "userId": 1,
          "yousignId": "string"
        }
      ],
      "offsetStart": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nbObjects` | number |  |
| `nbTotalObjects` | number |  |
| `objects` | array<object> |  |
| `objects[].askedAt` | date |  |
| `objects[].askedBy` | string |  |
| `objects[].email` | string |  |
| `objects[].firstName` | string |  |
| `objects[].id` | string |  |
| `objects[].lastName` | string |  |
| `objects[].link` | string |  |
| `objects[].phone` | string |  |
| `objects[].position` | number |  |
| `objects[].refuseAt` | string |  |
| `objects[].refuseReason` | string |  |
| `objects[].signatureId` | number |  |
| `objects[].signatureName` | string |  |
| `objects[].status` | string |  |
| `objects[].type` | string |  |
| `objects[].userId` | number |  |
| `objects[].yousignId` | string |  |
| `offsetStart` | number |  |

## Native endpoint

Through the native NetExplorer API, this operation is `GET /signatures/received` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-signatures-received.md) for the provider-specific parameters and requirements.

