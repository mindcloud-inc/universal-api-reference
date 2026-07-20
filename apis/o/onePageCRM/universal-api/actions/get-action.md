# OnePageCRM: Get Action

Retrieves an action from OnePageCRM.

```
GET https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/get-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnePageCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/get-action?connectionId=$CONNECTION_ID&actionId=69b027783c686ec82a8c6081" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "actionId": "69b027783c686ec82a8c6081"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/get-action?${params}`, {
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

Through the native OnePageCRM API, this operation is `GET /actions/:action_id` (base URL `https://app.onepagecrm.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-action.md) for the provider-specific parameters and requirements.

