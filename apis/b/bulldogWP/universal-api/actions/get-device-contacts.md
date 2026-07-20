# Bulldog-WP: List contacts

Retrieves contacts from Bulldog-WP.

```
GET https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-device-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bulldog-WP `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-device-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0&deviceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "deviceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-device-contacts?${params}`, {
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
      "broadcastId": "string",
      "channelId": "string",
      "chat": {},
      "countryCode": 1,
      "displayName": "Ava Chen",
      "formattedName": "Ava Chen",
      "formattedShortName": "Ava Chen",
      "groupId": "string",
      "name": "Ava Chen",
      "phone": "string",
      "shortName": "Ava Chen",
      "wid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `broadcastId` | string |  |
| `channelId` | string |  |
| `chat` | object |  |
| `countryCode` | number |  |
| `displayName` | string |  |
| `formattedName` | string |  |
| `formattedShortName` | string |  |
| `groupId` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `shortName` | string |  |
| `wid` | string |  |

## Native endpoint

Through the native Bulldog-WP API, this operation is `GET /chat/{deviceId}/contacts` (base URL `https://api.bulldog-wp.co.il/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-device-contacts.md) for the provider-specific parameters and requirements.

