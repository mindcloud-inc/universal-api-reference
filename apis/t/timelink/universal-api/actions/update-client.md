# Timelink: Update Client

Updates an existing client in Timelink.

```
PUT https://connect.mindcloud.co/v1/universal/timelink/latest/actions/update-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timelink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timelink/latest/actions/update-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timelink/latest/actions/update-client', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `name` | string | no |  |

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

Through the native Timelink API, this operation is `PATCH /clients/:id` (base URL `https://api.timelink.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-client.md) for the provider-specific parameters and requirements.

