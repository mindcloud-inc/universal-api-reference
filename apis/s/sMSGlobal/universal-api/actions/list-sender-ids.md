# SMSGlobal: List Sender IDs

Retrieves sender IDs from the SMSGlobal account.

```
GET https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/list-sender-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSGlobal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/list-sender-ids?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/list-sender-ids?${params}`, {
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
      "limit": 1,
      "offset": 1,
      "senderIds": [
        {
          "country": "string",
          "createdDate": "2026-05-07T12:00:00.000Z",
          "id": 1,
          "senderId": "string",
          "status": "string",
          "updatedDate": "2026-05-07T12:00:00.000Z"
        }
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `limit` | number | Number of sender ID objects returned. |
| `offset` | number | Pagination offset. |
| `senderIds[].country` | string | Sender ID country. |
| `senderIds[].createdDate` | date | Sender ID creation timestamp. |
| `senderIds[].id` | number | Sender ID identifier. |
| `senderIds[].senderId` | string | Sender ID value. |
| `senderIds[].status` | string | Sender ID status. |
| `senderIds[].updatedDate` | date | Sender ID update timestamp. |
| `total` | number | Total number of sender ID objects. |

## Native endpoint

Through the native SMSGlobal API, this operation is `GET /v2/sender-id` (base URL `https://api.smsglobal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sender-ids.md) for the provider-specific parameters and requirements.

