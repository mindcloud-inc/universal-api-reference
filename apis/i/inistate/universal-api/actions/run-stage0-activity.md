# Inistate: Run Stage0 Activity

Performs a Stage0 activity on an entry in Inistate.

```
PUT https://connect.mindcloud.co/v1/universal/inistate/latest/actions/run-stage0-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Inistate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/inistate/latest/actions/run-stage0-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "activityId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/inistate/latest/actions/run-stage0-activity', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "activityId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `activityId` | string | yes | Provider activity ID such as `Create` or `Edit`. |
| `payload` | object | no | Optional field payload keyed by provider field names. Default: `{}`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entryId` | number | no | Existing entry ID for edit or other entry-scoped activities. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activityId": "string",
      "collection": "string",
      "entryId": 1,
      "result": [
        {}
      ],
      "workspaceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activityId` | string | Executed activity identifier. |
| `collection` | string | Collection name. |
| `entryId` | number | Target entry ID when applicable. |
| `result` | array<object> | Entry payload(s) returned by the provider. |
| `workspaceId` | number | Workspace ID. |

## Native endpoint

Through the native Inistate API, this operation is `POST /api/activity` (base URL `https://api.inistate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-stage0-activity.md) for the provider-specific parameters and requirements.

