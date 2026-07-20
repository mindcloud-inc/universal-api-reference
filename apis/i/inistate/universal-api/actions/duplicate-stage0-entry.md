# Inistate: Duplicate Stage0 Entry

Creates a duplicated Stage0 entry in Inistate.

```
POST https://connect.mindcloud.co/v1/universal/inistate/latest/actions/duplicate-stage0-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Inistate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/inistate/latest/actions/duplicate-stage0-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entryId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/inistate/latest/actions/duplicate-stage0-entry', {
  method: 'POST',
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
| `entryId` | number | yes | Entry to duplicate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activityId": "string",
      "collection": "string",
      "entryId": 1,
      "id": 1,
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
| `entryId` | number | Source entry ID. |
| `id` | number | New duplicated entry ID. |
| `workspaceId` | number | Workspace ID. |

## Native endpoint

Through the native Inistate API, this operation is `POST /api/activity` (base URL `https://api.inistate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/duplicate-stage0-entry.md) for the provider-specific parameters and requirements.

