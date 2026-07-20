# Affinda: Get list of all workspaces

Retrieves all accessible workspaces from Affinda.

```
GET https://connect.mindcloud.co/v1/universal/affinda/latest/actions/list-workspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Affinda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/affinda/latest/actions/list-workspaces?connectionId=$CONNECTION_ID&organization=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organization": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/affinda/latest/actions/list-workspaces?${params}`, {
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
| `name` | string | no | Filter by name. |
| `organization` | string | yes | Filter by organization. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "collections": [
        {}
      ],
      "confirmedDocsCount": 1,
      "documentSplitter": {},
      "documentTypes": [
        "string"
      ],
      "identifier": "string",
      "ingestEmail": "ava@example.com",
      "members": [
        {}
      ],
      "name": "Ava Chen",
      "organization": {},
      "rejectDuplicates": true,
      "rejectInvalidDocuments": true,
      "unvalidatedDocsCount": 1,
      "visibility": "string",
      "whitelistIngestAddresses": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collections` | array<object> |  |
| `confirmedDocsCount` | number |  |
| `documentSplitter` | object |  |
| `documentTypes` | array<string> |  |
| `identifier` | string |  |
| `ingestEmail` | string |  |
| `members` | array<object> |  |
| `name` | string |  |
| `organization` | object |  |
| `rejectDuplicates` | boolean |  |
| `rejectInvalidDocuments` | boolean |  |
| `unvalidatedDocsCount` | number |  |
| `visibility` | string |  |
| `whitelistIngestAddresses` | array<string> |  |

## Native endpoint

Through the native Affinda API, this operation is `GET /v3/workspaces` (base URL `https://api.us1.affinda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspaces.md) for the provider-specific parameters and requirements.

