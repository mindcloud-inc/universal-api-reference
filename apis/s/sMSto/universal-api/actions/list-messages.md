# SMS.to: List Messages

Retrieves sent SMS messages from SMS.to.

```
GET https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/list-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS.to `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/list-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/list-messages?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Maximum number of messages per page. Default: `15`. |
| `orderDirection` | string | no | Sort direction. Default: `desc`. |
| `orderBy` | list<string> | no | Field to sort by. Accepted fields: created_at, id, sent_at, sender_id, is_api, status, cost. One of: `cost`, `created_at`, `id`, `is_api`, `sender_id`, `sent_at`, `status`. Default: `created_at`. |
| `status` | string | no | Filter by status. |
| `to` | string | no | Filter by recipient number. |
| `createdAtFrom` | date | no | Filter from date. Format: Y-m-d H:i:s. |
| `createdAtTo` | date | no | Filter to date. Format: Y-m-d H:i:s. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callbackUrl": "https://example.com",
      "campaignId": "string",
      "cost": 1,
      "createdAt": "string",
      "failedReason": "string",
      "id": "string",
      "internalFailedReason": "string",
      "isApi": true,
      "message": "string",
      "scheduledFor": "string",
      "senderId": "string",
      "sentAt": "string",
      "smsCount": 1,
      "status": "string",
      "timezone": "string",
      "to": "string",
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callbackUrl` | string |  |
| `campaignId` | string |  |
| `cost` | number |  |
| `createdAt` | string |  |
| `failedReason` | string |  |
| `id` | string |  |
| `internalFailedReason` | string |  |
| `isApi` | boolean |  |
| `message` | string |  |
| `scheduledFor` | string |  |
| `senderId` | string |  |
| `sentAt` | string |  |
| `smsCount` | number |  |
| `status` | string |  |
| `timezone` | string |  |
| `to` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native SMS.to API, this operation is `GET /v2/messages` (base URL `https://api.sms.to`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-messages.md) for the provider-specific parameters and requirements.

