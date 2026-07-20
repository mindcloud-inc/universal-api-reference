# Timelink: Get Service

Retrieves a service from the Timelink workspace.

```
GET https://connect.mindcloud.co/v1/universal/timelink/latest/actions/get-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timelink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timelink/latest/actions/get-service?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timelink/latest/actions/get-service?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acronym": {},
      "active": true,
      "billable": true,
      "color": "string",
      "companyId": "string",
      "createdAt": "string",
      "defaultTimeEntryDescription": {},
      "demoFlag": 1,
      "extToolId": "string",
      "id": "string",
      "imageId": {},
      "info": {},
      "lastSync": {},
      "name": "Ava Chen",
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
| `billable` | boolean |  |
| `color` | string |  |
| `companyId` | string |  |
| `createdAt` | string |  |
| `defaultTimeEntryDescription` | object |  |
| `demoFlag` | number |  |
| `extToolId` | string |  |
| `id` | string |  |
| `imageId` | object |  |
| `info` | object |  |
| `lastSync` | object |  |
| `name` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Timelink API, this operation is `GET /services/:id` (base URL `https://api.timelink.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-service.md) for the provider-specific parameters and requirements.

