# Recommand: List Documents

Retrieves document records from the Recommand API.

```
GET https://connect.mindcloud.co/v1/universal/recommand/latest/actions/list-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/list-documents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recommand/latest/actions/list-documents?${params}`, {
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
| `companyid` | string | no | companyId parameter. |
| `direction` | string | no | direction parameter. |
| `envelopeid` | string | no | envelopeId parameter. |
| `excludeattachments` | boolean | no | excludeAttachments parameter. |
| `from` | string | no | from parameter. |
| `isunread` | string | no | isUnread parameter. |
| `search` | string | no | search parameter. |
| `to` | string | no | to parameter. |
| `type` | string | no | type parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documents": [
        {
          "companyId": "string",
          "countryC1": "string",
          "createdAt": "string",
          "direction": "string",
          "docTypeId": "string",
          "emailRecipients": [
            "ava@example.com"
          ],
          "envelopeId": "string",
          "id": "string",
          "labels": [
            {}
          ],
          "parsed": {},
          "peppolConversationId": "string",
          "peppolMessageId": "string",
          "processId": "string",
          "readAt": "string",
          "receivedPeppolSignalMessage": "string",
          "receiverId": "string",
          "senderId": "string",
          "sentOverEmail": true,
          "sentOverPeppol": true,
          "teamId": "string",
          "type": "string",
          "updatedAt": "string",
          "validation": {}
        }
      ],
      "pagination": {
        "limit": 1,
        "page": 1,
        "total": 1,
        "totalPages": 1
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
| `documents` | array<object> |  |
| `documents[].companyId` | string |  |
| `documents[].countryC1` | string |  |
| `documents[].createdAt` | string |  |
| `documents[].direction` | string |  |
| `documents[].docTypeId` | string |  |
| `documents[].emailRecipients` | array<string> |  |
| `documents[].envelopeId` | string |  |
| `documents[].id` | string |  |
| `documents[].labels` | array<object> |  |
| `documents[].parsed` | object |  |
| `documents[].peppolConversationId` | string |  |
| `documents[].peppolMessageId` | string |  |
| `documents[].processId` | string |  |
| `documents[].readAt` | string |  |
| `documents[].receivedPeppolSignalMessage` | string |  |
| `documents[].receiverId` | string |  |
| `documents[].senderId` | string |  |
| `documents[].sentOverEmail` | boolean |  |
| `documents[].sentOverPeppol` | boolean |  |
| `documents[].teamId` | string |  |
| `documents[].type` | string |  |
| `documents[].updatedAt` | string |  |
| `documents[].validation` | object |  |
| `pagination` | object |  |
| `pagination.limit` | number |  |
| `pagination.page` | number |  |
| `pagination.total` | number |  |
| `pagination.totalPages` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Recommand API, this operation is `GET /api/v1/documents` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-documents.md) for the provider-specific parameters and requirements.

