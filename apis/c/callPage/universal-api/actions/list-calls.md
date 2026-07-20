# CallPage: List Calls

Retrieves call history records from CallPage.

```
GET https://connect.mindcloud.co/v1/universal/callPage/latest/actions/list-calls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallPage `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callPage/latest/actions/list-calls?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callPage/latest/actions/list-calls?${params}`, {
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
| `phoneNumber` | string | no | Filter by visitor phone number in E.164 format. Example: `+15551234567`. |
| `statuses` | list<string> | no | Filter by one or more call statuses. One of: `cancelled`, `completed`, `failed`, `in-progress`, `manager-failed`, `new`, `ringing`, `scheduled`, `user-failed`. Accepts multiple values as an array. Example: `completed`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `displayHidden` | number | no | Whether to include hidden calls. Example: `1`. |
| `callIds` | number<number> | no | Filter by one or more call IDs. Accepts multiple values as an array. Example: `10507595`. |
| `userIds` | number<number> | no | Filter by one or more user IDs. Accepts multiple values as an array. Example: `100447`. |
| `tagIds` | number<number> | no | Filter by one or more tag IDs. Accepts multiple values as an array. Example: `107`. |
| `dateFrom` | number | no | Start timestamp filter. Example: `1704067200`. |
| `dateTo` | number | no | End timestamp filter. Example: `1706745599`. |
| `widgetIds` | number<number> | no | Filter by one or more widget IDs. Accepts multiple values as an array. Example: `123`. |
| `url` | string | no | Filter by widget installation URL. Example: `https://example.com`. |
| `incomingNumberIds` | number<number> | no | Filter by one or more incoming number IDs. Accepts multiple values as an array. Example: `66`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "cancelled_at": "string",
        "created_at": "string",
        "human_status": "string",
        "id": 1,
        "leadable_description": "string",
        "scheduled_at": "string",
        "to": "string",
        "to_formatted": "string"
      },
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.cancelled_at` | string | When the call was cancelled, if applicable. |
| `data.created_at` | string | When the call request was created. |
| `data.human_status` | string | The human-readable call status. |
| `data.id` | number | The call identifier. |
| `data.leadable_description` | string | The leadable description. |
| `data.scheduled_at` | string | When the call is scheduled, if applicable. |
| `data.to` | string | The destination phone number. |
| `data.to_formatted` | string | The formatted destination phone number. |
| `id` | number | The top-level call record identifier. |

## Native endpoint

Through the native CallPage API, this operation is `GET https://core.callpage.io/api/v3/external/calls/history` (base URL `https://core.callpage.io/api/v1/external`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-calls.md) for the provider-specific parameters and requirements.

