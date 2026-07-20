# Affinda: Get specific workspace

Retrieves a specific workspace from Affinda.

```
GET https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Affinda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-workspace?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-workspace?${params}`, {
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
| `identifier` | string | yes | Workspace's identifier |

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

Through the native Affinda API, this operation is `GET /v3/workspaces/:identifier` (base URL `https://api.us1.affinda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace.md) for the provider-specific parameters and requirements.

