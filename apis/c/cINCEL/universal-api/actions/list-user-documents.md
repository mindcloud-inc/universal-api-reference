# CINCEL: List User Documents



```
GET https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/list-user-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CINCEL `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/list-user-documents?connectionId=$CONNECTION_ID&limit=25&offset=0&user=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "user": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/list-user-documents?${params}`, {
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
| `user` | number | yes | User ID from the path. |
| `q` | string | no | Full-text search query. |
| `nameLike` | string | no | Filter documents by name substring. |
| `status[]` | array<string> | no | Filter documents by status. |
| `feed` | string | no | Filter documents by feed bucket. |
| `inviteType[]` | array<string> | no | Filter documents by invite type. |
| `includeDeleted` | boolean | no | Include deleted documents. |
| `createdAtGte` | date | no | Only include documents created on or after this timestamp. |
| `createdAtLte` | date | no | Only include documents created on or before this timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "certified": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creationIp": "string",
      "creator": {},
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "disableEmails": true,
      "doc": "string",
      "folder": "string",
      "form": "string",
      "hideCertificatePii": true,
      "invites": [
        {}
      ],
      "name": "Ava Chen",
      "notifyCreator": true,
      "stage": 1,
      "status": "string",
      "team": "string",
      "transaction": "string",
      "trashedAt": "2026-05-07T12:00:00.000Z",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `certified` | boolean | Whether the document is certified. |
| `createdAt` | date | Document creation timestamp. |
| `creationIp` | string | IP address used during document creation. |
| `creator` | object | Document creator details. |
| `deletedAt` | date | Deletion timestamp when present. |
| `description` | string | Document description. |
| `disableEmails` | boolean | Whether document emails are disabled. |
| `doc` | string | Original document PDF URL. |
| `folder` | string | Folder UUID containing the document. |
| `form` | string | Associated form UUID when present. |
| `hideCertificatePii` | boolean | Whether certificate PII is hidden. |
| `invites` | array<object> | Invites associated with the document. |
| `name` | string | Document name. |
| `notifyCreator` | boolean | Whether the creator is notified when the document is signed. |
| `stage` | number | Current document stage. |
| `status` | string | Document status. |
| `team` | string | Owning team UUID. |
| `transaction` | string | Transaction UUID. |
| `trashedAt` | date | Trash timestamp when present. |
| `updatedAt` | date | Document update timestamp. |
| `uuid` | string | Document UUID. |

## Native endpoint

Through the native CINCEL API, this operation is `GET /users/:user/documents` (base URL `https://api.cincel.digital/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-user-documents.md) for the provider-specific parameters and requirements.

