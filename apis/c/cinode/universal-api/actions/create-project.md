# Cinode: Create Project

Creates a new project in Cinode.

```
POST https://connect.mindcloud.co/v1/universal/cinode/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cinode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cinode/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": 1,
  "title": "string",
  "customerId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cinode/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": 1,
    "title": "string",
    "customerId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | number | yes | Cinode company ID. |
| `title` | string | yes | Project title. |
| `customerId` | number | yes | Customer ID linked to the project. |
| `description` | string | no | Project description. |
| `internalId` | string | no | Internal project identifier. |
| `externalId` | string | no | External project identifier. |
| `estimatedCloseDate` | date | no | Estimated close date. |
| `estimatedValue` | number | no | Estimated project value. |
| `contractValue` | number | no | Contract value. |
| `probability` | number | no | Project probability. |
| `projectState` | number | no | Project state enum. 0=Open, 30=Won, 40=Lost, 50=Abandoned, 60=Suspended. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": 1,
      "contractValue": 1,
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "customerId": 1,
      "customerIdentifier": "string",
      "description": "string",
      "estimatedValue": 1,
      "externalId": "string",
      "id": 1,
      "identifier": "string",
      "internalId": "string",
      "lastTouchDateTime": "2026-05-07T12:00:00.000Z",
      "probability": 1,
      "seoId": "string",
      "title": "string",
      "updatedDateTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | number |  |
| `contractValue` | number |  |
| `createdDateTime` | date |  |
| `customerId` | number |  |
| `customerIdentifier` | string |  |
| `description` | string |  |
| `estimatedValue` | number |  |
| `externalId` | string |  |
| `id` | number |  |
| `identifier` | string |  |
| `internalId` | string |  |
| `lastTouchDateTime` | date |  |
| `probability` | number |  |
| `seoId` | string |  |
| `title` | string |  |
| `updatedDateTime` | date |  |

## Native endpoint

Through the native Cinode API, this operation is `POST /v0.1/companies/:companyId/projects` (base URL `https://api.cinode.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

