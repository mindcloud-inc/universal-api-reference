# Vybit: Get Log Entry



```
GET https://connect.mindcloud.co/v1/universal/vybit/latest/actions/get-log-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vybit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vybit/latest/actions/get-log-entry?connectionId=$CONNECTION_ID&logKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "logKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vybit/latest/actions/get-log-entry?${params}`, {
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
| `logKey` | string | yes | The unique key of the log entry. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "imageUrl": "https://example.com",
      "key": "string",
      "linkUrl": "https://example.com",
      "log": "string",
      "notification": "string",
      "ownerName": "Ava Chen",
      "senderName": "Ava Chen",
      "soundKey": "string",
      "vybDescription": "string",
      "vybfollowKey": "string",
      "vybKey": "string",
      "vybName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `imageUrl` | string |  |
| `key` | string |  |
| `linkUrl` | string |  |
| `log` | string |  |
| `notification` | string |  |
| `ownerName` | string |  |
| `senderName` | string |  |
| `soundKey` | string |  |
| `vybDescription` | string |  |
| `vybfollowKey` | string |  |
| `vybKey` | string |  |
| `vybName` | string |  |

## Native endpoint

Through the native Vybit API, this operation is `GET /log/{{logKey}}` (base URL `https://api.vybit.net/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-log-entry.md) for the provider-specific parameters and requirements.

