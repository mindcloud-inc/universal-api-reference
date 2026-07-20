# DialMyCalls: List Texts

Retrieves a list of texts from DialMyCalls.

```
GET https://connect.mindcloud.co/v1/universal/dialMyCalls/latest/actions/list-texts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DialMyCalls `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dialMyCalls/latest/actions/list-texts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dialMyCalls/latest/actions/list-texts?${params}`, {
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
      "accessaccountId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creditCost": 1,
      "id": "string",
      "name": "Ava Chen",
      "pendingCancel": true,
      "sendAt": "2026-05-07T12:00:00.000Z",
      "totalRecipients": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessaccountId` | string | Access account ID when applicable. |
| `createdAt` | date | When the broadcast was created. |
| `creditCost` | number | Credits used by the broadcast. |
| `id` | string | Text service ID. |
| `name` | string | Broadcast name. |
| `pendingCancel` | boolean | Whether cancelation is pending. |
| `sendAt` | date | Scheduled UTC send timestamp. |
| `totalRecipients` | number | Recipient count. |
| `updatedAt` | date | When the broadcast was last updated. |

## Native endpoint

Through the native DialMyCalls API, this operation is `GET /service/texts` (base URL `https://{{credentials.apiKey}}@api.dialmycalls.com/2.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-texts.md) for the provider-specific parameters and requirements.

