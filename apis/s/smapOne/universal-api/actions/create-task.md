# smapOne: Create task

Creates a new task in smapOne.

```
POST https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smapOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "smap_id": "string",
  "title": "string",
  "version": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "smap_id": "string",
    "title": "string",
    "version": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `comment` | string | no | Comment from the creator of the task. |
| `data` | object | no | Task prefill data object matching the smap schema. |
| `has_priority` | boolean | no | Whether the task is prioritized. |
| `smap_id` | string | yes | The smap id. |
| `title` | string | yes | Name of the task or data record. |
| `user_email` | string | no | User email to assign the task to. |
| `version` | string | yes | The smap version in major.minor format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "id": "string",
      "recordType": "string",
      "userEmail": "ava@example.com",
      "userName": "Ava Chen",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `id` | string |  |
| `recordType` | string |  |
| `userEmail` | string |  |
| `userName` | string |  |
| `version` | string |  |

## Native endpoint

Through the native smapOne API, this operation is `POST /preview/Smaps/{smapId}/Versions/{version}/Tasks` (base URL `https://platform.smapone.com/Backend`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

