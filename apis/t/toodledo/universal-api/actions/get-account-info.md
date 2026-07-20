# Toodledo: Get Account Info

Retrieves account details from Toodledo.

```
GET https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/get-account-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toodledo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/get-account-info?${params}`, {
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
      "alias": "string",
      "dateformat": 1,
      "email": "ava@example.com",
      "hidemonths": 1,
      "hotlistduedate": 1,
      "hotlistpriority": 1,
      "lastdelete_note": 1,
      "lastdelete_task": 1,
      "lastedit_context": 1,
      "lastedit_folder": 1,
      "lastedit_goal": 1,
      "lastedit_list": 1,
      "lastedit_location": 1,
      "lastedit_note": 1,
      "lastedit_outline": 1,
      "lastedit_task": 1,
      "pro": 1,
      "showtabnums": 1,
      "timezone": 1,
      "userid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string | User display name. |
| `dateformat` | number | Preferred date format option. |
| `email` | string | Login email address. |
| `hidemonths` | number | Months ahead when tasks are hidden. |
| `hotlistduedate` | number | Due date lead-time for hotlist inclusion. |
| `hotlistpriority` | number | Minimum priority for hotlist inclusion. |
| `lastdelete_note` | number | Last note delete timestamp. |
| `lastdelete_task` | number | Last task delete timestamp. |
| `lastedit_context` | number | Last context edit timestamp. |
| `lastedit_folder` | number | Last folder edit timestamp. |
| `lastedit_goal` | number | Last goal edit timestamp. |
| `lastedit_list` | number | Last list edit timestamp. |
| `lastedit_location` | number | Last location edit timestamp. |
| `lastedit_note` | number | Last note edit timestamp. |
| `lastedit_outline` | number | Last outline edit timestamp. |
| `lastedit_task` | number | Last task edit timestamp. |
| `pro` | number | Subscription tier indicator. |
| `showtabnums` | number | Whether tab numbers are shown. |
| `timezone` | number | Timezone offset in half-hours from server time. |
| `userid` | string | Unique identifier for the user. |

## Native endpoint

Through the native Toodledo API, this operation is `GET /account/get.php` (base URL `https://api.toodledo.com/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-info.md) for the provider-specific parameters and requirements.

