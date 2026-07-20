# GoDial: Get Task

Retrieves details for a task from GoDial.

```
GET https://connect.mindcloud.co/v1/universal/goDial/latest/actions/task-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoDial `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goDial/latest/actions/task-view?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goDial/latest/actions/task-view?${params}`, {
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
| `id` | string | yes | Task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountsId": "string",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "desc": "string",
      "done": true,
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountsId` | string |  |
| `createdOn` | date |  |
| `desc` | string |  |
| `done` | boolean |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native GoDial API, this operation is `GET /externals/tasks/[:id]/view` (base URL `https://enterprise.godial.cc/meta/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/task-view.md) for the provider-specific parameters and requirements.

