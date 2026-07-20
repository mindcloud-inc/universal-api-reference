# OnePageCRM: List Actions

Retrieves actions from OnePageCRM.

```
GET https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/list-actions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnePageCRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/list-actions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/list-actions?${params}`, {
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
| `done` | boolean | no | Only return completed actions. |
| `status` | list<string> | no | Return actions of a particular status. One of: `asap`, `date`, `date_time`, `done`, `queued`, `queued_with_date`, `waiting`. |
| `assigneeId` | string | no | Return actions assigned to a specific user. Example: `5aba36b19007ba0f570c9523`. |
| `contactId` | string | no | Return actions for a specific contact. Example: `5ae06ef9d55673108fe8877b`. |
| `companyId` | string | no | Return actions for a specific company. Example: `6se06df9d55673108re84745`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dateFilter` | list<string> | no | Choose which date field to use with Since or Until. One of: `close_date`, `created_at`, `date`, `modified_at`, `updated_at`. |
| `since` | date | no | Return actions added or edited since this date or timestamp. Example: `2018-07-01`. |
| `until` | date | no | Return actions added or edited until this date or timestamp. Example: `2018-07-31`. |
| `modifiedSince` | date | no | Return only actions modified since this date or timestamp. Example: `2018-07-01`. |
| `unmodifiedSince` | date | no | Return only actions unmodified since this date or timestamp. Example: `2018-07-01`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actions": [
        {
          "action": {
            "assigneeId": "string",
            "contactId": "string",
            "createdAt": "2026-05-07T12:00:00.000Z",
            "date": "2026-05-07T12:00:00.000Z",
            "done": true,
            "id": "string",
            "modifiedAt": "2026-05-07T12:00:00.000Z",
            "status": "string",
            "text": "string"
          }
        }
      ],
      "maxPage": 1,
      "page": 1,
      "perPage": 1,
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actions[].action.assigneeId` | string |  |
| `actions[].action.contactId` | string |  |
| `actions[].action.createdAt` | date |  |
| `actions[].action.date` | date |  |
| `actions[].action.done` | boolean |  |
| `actions[].action.id` | string |  |
| `actions[].action.modifiedAt` | date |  |
| `actions[].action.status` | string |  |
| `actions[].action.text` | string |  |
| `maxPage` | number |  |
| `page` | number |  |
| `perPage` | number |  |
| `totalCount` | number |  |

## Native endpoint

Through the native OnePageCRM API, this operation is `GET /actions` (base URL `https://app.onepagecrm.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-actions.md) for the provider-specific parameters and requirements.

