# Microsoft 365: List Calendars

Retrieves calendars from Microsoft 365.

```
GET https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/list-calendars
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/list-calendars?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/list-calendars?${params}`, {
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
| `canEdit` | boolean |  |
| `canShare` | boolean |  |
| `color` | string |  |
| `id` | string |  |
| `isDefaultCalendar` | boolean |  |
| `isRemovable` | boolean |  |
| `name` | string |  |
| `owner.address` | string |  |
| `owner.name` | string |  |

## Native endpoint

Through the native Microsoft 365 API, this operation is `GET /v1.0/me/calendars` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-calendars.md) for the provider-specific parameters and requirements.

