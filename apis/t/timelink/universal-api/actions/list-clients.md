# Timelink: List Clients

Retrieves clients from the Timelink workspace.

```
GET https://connect.mindcloud.co/v1/universal/timelink/latest/actions/list-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timelink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timelink/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timelink/latest/actions/list-clients?${params}`, {
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
| `search` | string | no |  |

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

Through the native Timelink API, this operation is `GET /clients` (base URL `https://api.timelink.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-clients.md) for the provider-specific parameters and requirements.

