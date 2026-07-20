# Microsoft 365 Calendar: List Calendars

Retrieves calendars from Microsoft 365 Calendar.

```
GET https://connect.mindcloud.co/v1/universal/microsoft365Calendar/latest/actions/list-calendars
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365Calendar/latest/actions/list-calendars?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365Calendar/latest/actions/list-calendars?${params}`, {
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
      "canEdit": true,
      "canShare": true,
      "color": "string",
      "id": "string",
      "isDefaultCalendar": true,
      "isRemovable": true,
      "name": "Ava Chen",
      "owner": {
        "address": "string",
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canEdit` | boolean | Whether the signed-in user can edit the calendar. |
| `canShare` | boolean | Whether the signed-in user can share the calendar. |
| `color` | string | Calendar color. |
| `id` | string | Calendar ID. |
| `isDefaultCalendar` | boolean | Whether this is the default calendar. |
| `isRemovable` | boolean | Whether the calendar can be removed. |
| `name` | string | Calendar display name. |
| `owner.address` | string | Calendar owner email address. |
| `owner.name` | string | Calendar owner display name. |

## Native endpoint

Through the native Microsoft 365 Calendar API, this operation is `GET /v1.0/me/calendars` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-calendars.md) for the provider-specific parameters and requirements.

