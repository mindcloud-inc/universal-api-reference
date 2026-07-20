# Recommand: Create Company Document Type

Creates a new company document type in Recommand.

```
POST https://connect.mindcloud.co/v1/universal/recommand/latest/actions/create-company-document-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/create-company-document-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyid": "string",
  "doctypeid": "string",
  "processid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recommand/latest/actions/create-company-document-type', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyid": "string",
    "doctypeid": "string",
    "processid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyid` | string | yes | companyId parameter. |
| `doctypeid` | string | yes | The ID of the document type to create |
| `processid` | string | yes | The ID of the process to create |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentType": {
        "companyId": "string",
        "createdAt": "string",
        "docTypeId": "string",
        "id": "string",
        "processId": "string",
        "updatedAt": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentType` | object |  |
| `documentType.companyId` | string |  |
| `documentType.createdAt` | string |  |
| `documentType.docTypeId` | string |  |
| `documentType.id` | string |  |
| `documentType.processId` | string |  |
| `documentType.updatedAt` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Recommand API, this operation is `POST /api/v1/companies/:companyId/document-types` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company-document-type.md) for the provider-specific parameters and requirements.

