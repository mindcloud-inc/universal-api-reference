# Natif.ai Universal API Examples

These examples use the MindCloud API key and Natif.ai connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Available Workflows

Retrieves available processing workflows from Natif.ai.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/natifai/latest/actions/list-available-workflows?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/natifai/latest/actions/list-available-workflows?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "accessible_child_workflows": [
        "string"
      ],
      "any_child_deidentified": true,
      "beta": true,
      "category": "string",
      "character_set": "string",
      "customer_id": "string",
      "description": "string",
      "image": "string",
      "is_latest_architecture": true,
      "kind": "string",
      "last_training_date": "2026-05-07T12:00:00.000Z",
      "locked": true,
      "long_description": "string",
      "migration_due_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "num_of_deeper_descendant_workflows": 1,
      "num_of_inaccessible_child_workflows": 1,
      "parent_model_ahead": true,
      "parent_workflow_id": "string",
      "permissions": [
        "string"
      ],
      "preview": true,
      "retrievable_results": [
        "string"
      ],
      "shareable": true,
      "tags": [
        {}
      ],
      "training_state": "string",
      "visibility": "string",
      "workflow_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Available Workflows action reference](actions/list-available-workflows.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/natifai/latest/actions/list-available-workflows).

## Create Document Share Token

Creates a document sharing token in Natif.ai.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/natifai/latest/actions/create-document-share-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string",
  "expiresAt": "2026-04-14"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/natifai/latest/actions/create-document-share-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "string",
    "expiresAt": "2026-04-14"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "document_id": "string",
      "expires_at": "2026-05-07T12:00:00.000Z",
      "issuer_user_id": "string",
      "last_used_at": "2026-05-07T12:00:00.000Z",
      "tenant_id": "string",
      "token": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Document Share Token action reference](actions/create-document-share-token.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/natifai/latest/actions/create-document-share-token).
