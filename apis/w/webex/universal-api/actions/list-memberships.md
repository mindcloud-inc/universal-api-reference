# Webex: List Memberships

Lists memberships in your Webex account.

```
GET https://connect.mindcloud.co/v1/universal/webex/latest/actions/list-memberships
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webex/latest/actions/list-memberships?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webex/latest/actions/list-memberships?${params}`, {
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
| `max` | number | no | Maximum number of memberships to return. Example: `50`. |
| `roomId` | string | no | Filter memberships to one room. Example: `Y2lzY29zcGFyazovL3VzL1JPT00v...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isModerator": true,
      "isMonitor": true,
      "isRoomHidden": true,
      "personDisplayName": "Ava Chen",
      "personEmail": "ava@example.com",
      "personId": "string",
      "personOrgId": "string",
      "roomId": "string",
      "roomType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date | Membership creation timestamp. |
| `id` | string | Membership identifier. |
| `isModerator` | boolean | Whether the member is a moderator. |
| `isMonitor` | boolean | Whether the member is a monitor. |
| `isRoomHidden` | boolean | Whether the room is hidden for the member. |
| `personDisplayName` | string | Display name for the member. |
| `personEmail` | string | Email address for the member. |
| `personId` | string | Person identifier for the member. |
| `personOrgId` | string | Organization identifier for the member. |
| `roomId` | string | Room associated with the membership. |
| `roomType` | string | Type of room associated with the membership. |

## Native endpoint

Through the native Webex API, this operation is `GET /memberships` (base URL `https://webexapis.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-memberships.md) for the provider-specific parameters and requirements.

