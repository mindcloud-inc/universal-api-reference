# Inistate: Update Stage0 Entry

Updates an existing Stage0 entry in Inistate.

```
PUT https://connect.mindcloud.co/v1/universal/inistate/latest/actions/update-stage0-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Inistate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/inistate/latest/actions/update-stage0-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entryId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/inistate/latest/actions/update-stage0-entry', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entryId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entryId` | number | yes | Entry to update. |
| `payload` | object | no | Optional field payload keyed by provider field names. An empty object performs the provider's default edit submission shape verified in this run. Default: `{}`. |

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
| `entryId` | number | Updated entry ID. |
| `result` | array<object> | Updated entry payload(s) returned by the provider. |
| `workspaceId` | number | Workspace ID. |

## Native endpoint

Through the native Inistate API, this operation is `POST /api/activity` (base URL `https://api.inistate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-stage0-entry.md) for the provider-specific parameters and requirements.

