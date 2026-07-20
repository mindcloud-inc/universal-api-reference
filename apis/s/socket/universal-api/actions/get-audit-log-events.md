# Socket: Get Audit Log Events

Retrieves audit log events from Socket.

```
GET https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-audit-log-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-audit-log-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-audit-log-events?${params}`, {
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
      "nextPage": "string",
      "results": [
        {
          "countryCode": "string",
          "createdAt": "string",
          "eventId": "string",
          "ipAddress": "string",
          "organizationId": "string",
          "organizationName": "Ava Chen",
          "payload": {},
          "statusCode": 1,
          "type": "string",
          "updatedAt": "string",
          "userAgent": "string",
          "userEmail": "ava@example.com",
          "userId": "string",
          "userImage": "string"
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
| `nextPage` | string |  |
| `results` | array<object> |  |
| `results[]` | object |  |
| `results[].countryCode` | string |  |
| `results[].createdAt` | string |  |
| `results[].eventId` | string |  |
| `results[].ipAddress` | string |  |
| `results[].organizationId` | string |  |
| `results[].organizationName` | string |  |
| `results[].payload` | object |  |
| `results[].statusCode` | number |  |
| `results[].type` | string |  |
| `results[].updatedAt` | string |  |
| `results[].userAgent` | string |  |
| `results[].userEmail` | string |  |
| `results[].userId` | string |  |
| `results[].userImage` | string |  |

## Native endpoint

Through the native Socket API, this operation is `GET /orgs/:org_slug/audit-log` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-audit-log-events.md) for the provider-specific parameters and requirements.

