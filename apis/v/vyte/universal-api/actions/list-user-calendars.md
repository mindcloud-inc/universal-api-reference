# Vyte: List User Calendars

Retrieves a user's calendars from Vyte.

```
GET https://connect.mindcloud.co/v1/universal/vyte/latest/actions/list-user-calendars
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vyte `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vyte/latest/actions/list-user-calendars?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vyte/latest/actions/list-user-calendars?${params}`, {
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
| `userId` | string | no | The Vyte user ID. Default: `69ca9fead310017cb903a0fd`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "belongs_to": "string",
      "calendars": [
        {}
      ],
      "default_calendar": {},
      "sync_suggestions": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `belongs_to` | string |  |
| `calendars` | array<object> |  |
| `default_calendar` | object |  |
| `sync_suggestions` | boolean |  |

## Native endpoint

Through the native Vyte API, this operation is `GET v2/users/:user_id/calendars` (base URL `https://api.vyte.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-calendars.md) for the provider-specific parameters and requirements.

