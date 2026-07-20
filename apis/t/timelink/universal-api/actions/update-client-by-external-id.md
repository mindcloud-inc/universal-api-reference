# Timelink: Update Client by External ID

Updates an existing client in Timelink by external ID.

```
PUT https://connect.mindcloud.co/v1/universal/timelink/latest/actions/update-client-by-external-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timelink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timelink/latest/actions/update-client-by-external-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "extId": "stage3-client-001"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timelink/latest/actions/update-client-by-external-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "extId": "stage3-client-001"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `extId` | string | yes | The external reference ID for the client. Example: `stage3-client-001`. |
| `name` | string | no | Updated client name. Example: `Updated Client Name`. |
| `active` | boolean | no | Whether the client remains active. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acronym": {},
      "active": true,
      "activeProjectsCount": 1,
      "billable": true,
      "color": "string",
      "companyId": "string",
      "createdAt": "string",
      "demoFlag": true,
      "extToolId": "string",
      "id": "string",
      "imageId": {},
      "info": {},
      "lastSync": {},
      "name": "Ava Chen",
      "projectsCount": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acronym` | object |  |
| `active` | boolean |  |
| `activeProjectsCount` | number |  |
| `billable` | boolean |  |
| `color` | string |  |
| `companyId` | string |  |
| `createdAt` | string |  |
| `demoFlag` | boolean |  |
| `extToolId` | string |  |
| `id` | string |  |
| `imageId` | object |  |
| `info` | object |  |
| `lastSync` | object |  |
| `name` | string |  |
| `projectsCount` | number |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Timelink API, this operation is `PATCH /clients/ext/:extId` (base URL `https://api.timelink.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-client-by-external-id.md) for the provider-specific parameters and requirements.

