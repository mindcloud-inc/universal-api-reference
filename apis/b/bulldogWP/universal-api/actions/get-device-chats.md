# Bulldog-WP: Search chats

Finds chats in Bulldog-WP.

```
GET https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-device-chats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bulldog-WP `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-device-chats?connectionId=$CONNECTION_ID&limit=25&offset=0&deviceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "deviceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-device-chats?${params}`, {
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
| `deviceId` | string | yes | WhatsApp number device ID from Bulldog WP. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "kind": "string",
      "lid": "string",
      "name": "Ava Chen",
      "owner": {},
      "prevStatusUpdatedAt": "2026-05-07T12:00:00.000Z",
      "status": 1,
      "statusUpdatedAt": "2026-05-07T12:00:00.000Z",
      "statusUpdatedBy": {},
      "waStatus": "string",
      "wid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date |  |
| `expiresAt` | date |  |
| `kind` | string |  |
| `lid` | string |  |
| `name` | string |  |
| `owner` | object |  |
| `prevStatusUpdatedAt` | date |  |
| `status` | number |  |
| `statusUpdatedAt` | date |  |
| `statusUpdatedBy` | object |  |
| `waStatus` | string |  |
| `wid` | string |  |

## Native endpoint

Through the native Bulldog-WP API, this operation is `GET /chat/{deviceId}/chats` (base URL `https://api.bulldog-wp.co.il/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-device-chats.md) for the provider-specific parameters and requirements.

