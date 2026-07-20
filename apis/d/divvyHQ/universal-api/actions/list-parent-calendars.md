# DivvyHQ: List Parent Calendars



```
GET https://connect.mindcloud.co/v1/universal/divvyHQ/latest/actions/list-parent-calendars
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DivvyHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/divvyHQ/latest/actions/list-parent-calendars?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/divvyHQ/latest/actions/list-parent-calendars?${params}`, {
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
      "account": 1,
      "defaultDeadlineTime": "string",
      "editable": true,
      "id": 1,
      "isEnterprise": true,
      "isHidden": true,
      "kind": "string",
      "name": "Ava Chen",
      "parentCalendar": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | number | The Divvy account id. |
| `defaultDeadlineTime` | string | The default deadline time. |
| `editable` | boolean | Whether the calendar is editable. |
| `id` | number | The calendar id. |
| `isEnterprise` | boolean | Whether the calendar is enterprise scoped. |
| `isHidden` | boolean | Whether the calendar is hidden. |
| `kind` | string | The calendar kind. |
| `name` | string | The calendar name. |
| `parentCalendar` | number | The parent calendar id when present. |

## Native endpoint

Through the native DivvyHQ API, this operation is `GET /parentcalendars/` (base URL `https://app.divvyhq.com/api/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-parent-calendars.md) for the provider-specific parameters and requirements.

