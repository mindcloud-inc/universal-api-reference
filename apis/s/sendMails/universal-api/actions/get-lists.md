# SendMails: Get Lists

Retrieves a list of lists from SendMails.

```
GET https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/get-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendMails `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/get-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/get-lists?${params}`, {
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
      "clickRate": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fromEmail": "ava@example.com",
      "fromName": "Ava Chen",
      "id": 1,
      "name": "Ava Chen",
      "openRate": "string",
      "subscribers": "string",
      "uid": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clickRate` | string |  |
| `createdAt` | date |  |
| `fromEmail` | string |  |
| `fromName` | string |  |
| `id` | number |  |
| `name` | string |  |
| `openRate` | string |  |
| `subscribers` | string |  |
| `uid` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native SendMails API, this operation is `GET /lists` (base URL `https://app.sendmails.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lists.md) for the provider-specific parameters and requirements.

