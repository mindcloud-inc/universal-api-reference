# Week Plan: Delete Recurrence Exception



```
DELETE https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/delete-recurrence-exception
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Week Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/delete-recurrence-exception?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/delete-recurrence-exception?${params}`, {
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
      "ActionId": 1,
      "Date": "string",
      "RecurrenceId": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ActionId` | number |  |
| `Date` | string |  |
| `RecurrenceId` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Week Plan API, this operation is `DELETE recurrences/:recurrenceId/exceptions` (base URL `https://api.weekplan.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-recurrence-exception.md) for the provider-specific parameters and requirements.

