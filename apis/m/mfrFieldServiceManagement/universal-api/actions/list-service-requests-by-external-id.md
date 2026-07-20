# mfr Field Service Management: List Service Requests by External ID

Finds service requests in mfr Field Service Management by external ID.

```
GET https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/list-service-requests-by-external-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mfr Field Service Management `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/list-service-requests-by-external-id?connectionId=$CONNECTION_ID&externalId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "externalId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/list-service-requests-by-external-id?${params}`, {
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
| `externalId` | string | yes |  |

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

Through the native mfr Field Service Management API, this operation is `GET ServiceRequests?$filter=ExternalId eq '{{externalId}}'` (base URL `https://portal.mobilefieldreport.com/odata`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-service-requests-by-external-id.md) for the provider-specific parameters and requirements.

