# OnePageCRM: Mark Action as Done

Marks an action as done in OnePageCRM.

```
PUT https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/mark-action-as-done
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnePageCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/mark-action-as-done" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "actionId": "69b027783c686ec82a8c6081"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/mark-action-as-done', {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigneeId": "string",
      "contactId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "done": true,
      "doneAt": "2026-05-07T12:00:00.000Z",
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
| `done` | boolean |  |
| `doneAt` | date |  |
| `id` | string |  |
| `modifiedAt` | date |  |
| `status` | string |  |
| `text` | string |  |

## Native endpoint

Through the native OnePageCRM API, this operation is `PUT /actions/:action_id/mark_as_done` (base URL `https://app.onepagecrm.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-action-as-done.md) for the provider-specific parameters and requirements.

