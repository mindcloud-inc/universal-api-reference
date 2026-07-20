# Zoho Sprints: Move Item

Moves items to another sprint in Zoho Sprints.

```
PUT https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/move-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sprints `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/move-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string",
  "projectId": "string",
  "sprintId": "string",
  "itemidarr": "string",
  "tosprintid": "string",
  "toprojectid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/move-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string",
    "projectId": "string",
    "sprintId": "string",
    "itemidarr": "string",
    "tosprintid": "string",
    "toprojectid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | yes |  |
| `projectId` | string | yes |  |
| `sprintId` | string | yes |  |
| `itemidarr` | string | yes |  |
| `tosprintid` | string | yes |  |
| `toprojectid` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "itemIds": [
        "string"
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `itemIds` | array<string> |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Sprints API, this operation is `POST /team/:teamId/projects/:projectId/sprints/:sprintId/bulkupdate/` (base URL `https://sprintsapi.zoho.com/zsapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-item.md) for the provider-specific parameters and requirements.

