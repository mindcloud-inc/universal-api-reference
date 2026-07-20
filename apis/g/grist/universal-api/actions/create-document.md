# Grist: Create Document

Creates a new document in Grist.

```
POST https://connect.mindcloud.co/v1/universal/grist/latest/actions/create-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/grist/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": 1,
  "name": "Test Document from MindCloud"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/grist/latest/actions/create-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": 1,
    "name": "Test Document from MindCloud"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<number> | yes | Workspace ID |
| `name` | string | yes | Document name Default: `Test Document from MindCloud`. |
| `isPinned` | boolean | no | Whether to pin the document |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Grist API, this operation is `POST /workspaces/:workspaceId/docs` (base URL `https://docs.getgrist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document.md) for the provider-specific parameters and requirements.

