# Zoho Sprints: Get Project Status

Retrieves project item statuses from Zoho Sprints.

```
GET https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/get-project-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sprints `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/get-project-status?connectionId=$CONNECTION_ID&teamId=string&projectId=string&index=1&range=10" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string",
  "projectId": "string",
  "index": "1",
  "range": "10"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/get-project-status?${params}`, {
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
| `teamId` | string | yes |  |
| `projectId` | string | yes |  |
| `index` | number | yes | Default: `1`. |
| `range` | number | yes | Default: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hasCustomStatusAvailable": true,
      "hasPermission_customStatus": true,
      "isDefault": true,
      "status": "string",
      "status_prop": {},
      "statusIds": [
        "string"
      ],
      "statusJObj": {},
      "userDisplayName": {},
      "wipType": 1,
      "workflowId": "string",
      "workflowName": "Ava Chen",
      "zsuserIdvsZUID": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hasCustomStatusAvailable` | boolean |  |
| `hasPermission_customStatus` | boolean |  |
| `isDefault` | boolean |  |
| `status` | string |  |
| `status_prop` | object |  |
| `statusIds` | array<string> |  |
| `statusJObj` | object |  |
| `userDisplayName` | object |  |
| `wipType` | number |  |
| `workflowId` | string |  |
| `workflowName` | string |  |
| `zsuserIdvsZUID` | object |  |

## Native endpoint

Through the native Zoho Sprints API, this operation is `GET /team/:teamId/projects/:projectId/itemstatus/` (base URL `https://sprintsapi.zoho.com/zsapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-status.md) for the provider-specific parameters and requirements.

