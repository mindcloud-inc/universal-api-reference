# Meisterplan: List Calendars

Retrieves a list of calendars from Meisterplan.

```
GET https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/list-calendars
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meisterplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/list-calendars?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/list-calendars?${params}`, {
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
      "id": "string",
      "name": "Ava Chen",
      "parentId": "string",
      "path": "string",
      "workingHours": {
        "friday": 1,
        "monday": 1,
        "saturday": 1,
        "sunday": 1,
        "thursday": 1,
        "tuesday": 1,
        "wednesday": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Calendar ID |
| `name` | string | Calendar name |
| `parentId` | string | Parent calendar ID |
| `path` | string | Calendar path |
| `workingHours.friday` | number | Friday working hours |
| `workingHours.monday` | number | Monday working hours |
| `workingHours.saturday` | number | Saturday working hours |
| `workingHours.sunday` | number | Sunday working hours |
| `workingHours.thursday` | number | Thursday working hours |
| `workingHours.tuesday` | number | Tuesday working hours |
| `workingHours.wednesday` | number | Wednesday working hours |

## Native endpoint

Through the native Meisterplan API, this operation is `GET /calendars` (base URL `https://api.us.meisterplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-calendars.md) for the provider-specific parameters and requirements.

