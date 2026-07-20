# Vybit: List All Logs



```
GET https://connect.mindcloud.co/v1/universal/vybit/latest/actions/list-all-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vybit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vybit/latest/actions/list-all-logs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vybit/latest/actions/list-all-logs?${params}`, {
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
| `limit` | number | no | Maximum number of records to return |
| `offset` | number | no | Number of records to skip for pagination |
| `search` | string | no | Text search query |

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

Through the native Vybit API, this operation is `GET /logs` (base URL `https://api.vybit.net/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-logs.md) for the provider-specific parameters and requirements.

