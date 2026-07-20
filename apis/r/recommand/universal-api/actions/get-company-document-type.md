# Recommand: Get Company Document Type

Retrieves a company document type from Recommand.

```
GET https://connect.mindcloud.co/v1/universal/recommand/latest/actions/get-company-document-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/get-company-document-type?connectionId=$CONNECTION_ID&companyid=string&documenttypeid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyid": "string",
  "documenttypeid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recommand/latest/actions/get-company-document-type?${params}`, {
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
| `companyid` | string | yes | companyId parameter. |
| `documenttypeid` | string | yes | documentTypeId parameter. |

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

Through the native Recommand API, this operation is `GET /api/v1/companies/:companyId/document-types/:documentTypeId` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-document-type.md) for the provider-specific parameters and requirements.

