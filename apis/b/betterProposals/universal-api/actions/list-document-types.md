# Better Proposals: List Document Types

Retrieves document types from Better Proposals.

```
GET https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/list-document-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Proposals `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/list-document-types?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/list-document-types?${params}`, {
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
| `page` | number | no | Page number. Default: 1. Default: `1`. |
| `perPage` | number | no | Results per page. Default: 10. Default: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "numberOfOutstandingDocuments": 1,
      "numberOfTemplates": 1,
      "typeColour": "string",
      "typeIcon": "string",
      "typeName": "Ava Chen",
      "typeNameSingular": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `numberOfOutstandingDocuments` | number |  |
| `numberOfTemplates` | number |  |
| `typeColour` | string |  |
| `typeIcon` | string |  |
| `typeName` | string |  |
| `typeNameSingular` | string |  |

## Native endpoint

Through the native Better Proposals API, this operation is `GET /doctype` (base URL `https://api.betterproposals.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-document-types.md) for the provider-specific parameters and requirements.

