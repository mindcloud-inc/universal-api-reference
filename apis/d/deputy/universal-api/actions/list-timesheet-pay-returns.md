# Deputy: List Timesheet Pay Returns

Retrieves timesheet pay returns from Deputy.

```
GET https://connect.mindcloud.co/v1/universal/deputy/latest/actions/list-timesheet-pay-returns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deputy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deputy/latest/actions/list-timesheet-pay-returns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deputy/latest/actions/list-timesheet-pay-returns?${params}`, {
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
      "cost": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "creator": 1,
      "id": 1,
      "modified": "2026-05-07T12:00:00.000Z",
      "overridden": true,
      "overrideComment": "string",
      "payRule": 1,
      "timesheet": 1,
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cost` | number |  |
| `created` | date |  |
| `creator` | number |  |
| `id` | number |  |
| `modified` | date |  |
| `overridden` | boolean |  |
| `overrideComment` | string |  |
| `payRule` | number |  |
| `timesheet` | number |  |
| `value` | number |  |

## Native endpoint

Through the native Deputy API, this operation is `POST /api/v1/resource/TimesheetPayReturn/QUERY` (base URL `https://{{credentials.endpoint}}.deputy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-timesheet-pay-returns.md) for the provider-specific parameters and requirements.

