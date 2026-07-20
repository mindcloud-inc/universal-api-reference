# Recommand: List Company Document Types

Retrieves company document types from Recommand.

```
GET https://connect.mindcloud.co/v1/universal/recommand/latest/actions/list-company-document-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/list-company-document-types?connectionId=$CONNECTION_ID&limit=25&offset=0&companyid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "companyid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recommand/latest/actions/list-company-document-types?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentTypes": [
        {
          "companyId": "string",
          "createdAt": "string",
          "docTypeId": "string",
          "id": "string",
          "processId": "string",
          "updatedAt": "string"
        }
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentTypes` | array<object> |  |
| `documentTypes[].companyId` | string |  |
| `documentTypes[].createdAt` | string |  |
| `documentTypes[].docTypeId` | string |  |
| `documentTypes[].id` | string |  |
| `documentTypes[].processId` | string |  |
| `documentTypes[].updatedAt` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Recommand API, this operation is `GET /api/v1/companies/:companyId/document-types` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-company-document-types.md) for the provider-specific parameters and requirements.

