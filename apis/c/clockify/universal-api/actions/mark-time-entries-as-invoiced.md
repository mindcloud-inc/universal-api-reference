# Clockify: Mark Time Entries as Invoiced

Marks time entries as invoiced in Clockify.

```
PUT https://connect.mindcloud.co/v1/universal/clockify/latest/actions/mark-time-entries-as-invoiced
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/mark-time-entries-as-invoiced" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "invoiced": "true",
  "timeEntryIds[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/mark-time-entries-as-invoiced', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "invoiced": "true",
    "timeEntryIds[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<string> | yes |  |
| `invoiced` | boolean | yes | Example: `true`. |
| `timeEntryIds[]` | array<object> | yes |  |
| `timeEntryIds[].dateOfCreationFromObjectId` | date | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "invoiced": true,
      "timeEntryIds": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `invoiced` | boolean | Whether the selected time entries are marked as invoiced. |
| `timeEntryIds` | array<string> | The time entry identifiers that were updated. |

## Native endpoint

Through the native Clockify API, this operation is `PATCH workspaces/:workspaceId/time-entries/invoiced` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-time-entries-as-invoiced.md) for the provider-specific parameters and requirements.

