# mfr Field Service Management: Find Service Request by ID

Finds a service request in mfr Field Service Management by ID.

```
GET https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/find-service-request-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mfr Field Service Management `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/find-service-request-by-id?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/find-service-request-by-id?${params}`, {
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
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "closedAt": "string",
      "costCenterId": "string",
      "createFromServiceRequestTemplateId": "string",
      "currentOwnerId": 1,
      "customerId": 1,
      "customValues": [
        {}
      ],
      "dateModified": "2026-05-07T12:00:00.000Z",
      "dateOfCreation": "string",
      "description": "string",
      "externalId": "string",
      "id": 1,
      "isTemplate": true,
      "isTemplateMobile": true,
      "location": {},
      "name": "Ava Chen",
      "parentServiceRequestId": "string",
      "portalLink": "https://example.com",
      "releasedAt": "string",
      "state": "string",
      "targetTimeInMinutes": "string",
      "type": "string",
      "version": 1,
      "workDoneAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `closedAt` | string |  |
| `costCenterId` | string |  |
| `createFromServiceRequestTemplateId` | string |  |
| `currentOwnerId` | number |  |
| `customerId` | number |  |
| `customValues` | array<object> |  |
| `dateModified` | date |  |
| `dateOfCreation` | string |  |
| `description` | string |  |
| `externalId` | string |  |
| `id` | number |  |
| `isTemplate` | boolean |  |
| `isTemplateMobile` | boolean |  |
| `location` | object |  |
| `name` | string |  |
| `parentServiceRequestId` | string |  |
| `portalLink` | string |  |
| `releasedAt` | string |  |
| `state` | string |  |
| `targetTimeInMinutes` | string |  |
| `type` | string |  |
| `version` | number |  |
| `workDoneAt` | string |  |

## Native endpoint

Through the native mfr Field Service Management API, this operation is `GET ServiceRequests?$filter=Id eq {{id}}L` (base URL `https://portal.mobilefieldreport.com/odata`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-service-request-by-id.md) for the provider-specific parameters and requirements.

