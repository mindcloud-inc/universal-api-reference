# OnePageCRM: Update Action

Updates an existing action in OnePageCRM.

```
PUT https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/update-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnePageCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/update-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "actionId": "69b027783c686ec82a8c6081"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/update-action', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "actionId": "69b027783c686ec82a8c6081"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `actionId` | string | yes | Action ID. Example: `69b027783c686ec82a8c6081`. |
| `contactId` | string | no | ID of the contact associated with the action. Example: `5aba31ea9007ba0f570c92d4`. |
| `text` | string | no | The main text or description of the action. Example: `#1 Email Jane introducing our organization`. |
| `status` | list<string> | no | Status of the action. One of: `asap`, `date`, `date_time`, `done`, `queued`, `queued_with_date`, `waiting`. Default: `date`. |
| `date` | string | no | Due date for the action in YYYY-MM-DD format. Example: `2026-03-10`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `done` | boolean | no | Mark the action as complete. |
| `exactTime` | date | no | UNIX epoch time in seconds when the action is due. Example: `2018-05-16T12:00:00Z`. |
| `assigneeId` | string | no | ID of the user assigned to the action. Example: `5aaa9b009007ba08c9ebaef7`. |
| `position` | number | no | Position of the action in the queued actions list. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assigneeId` | string |  |
| `contactId` | string |  |
| `createdAt` | date |  |
| `date` | date |  |
| `done` | boolean |  |
| `id` | string |  |
| `modifiedAt` | date |  |
| `status` | string |  |
| `text` | string |  |

## Native endpoint

Through the native OnePageCRM API, this operation is `PUT /actions/:action_id` (base URL `https://app.onepagecrm.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-action.md) for the provider-specific parameters and requirements.

