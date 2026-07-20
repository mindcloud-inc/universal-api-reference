# Unbounce: Create Lead Deletion Request

Creates an asynchronous lead deletion request in Unbounce.

```
POST https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/create-lead-deletion-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unbounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/create-lead-deletion-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "page_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/create-lead-deletion-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "page_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `lead_ids` | string | no | Lead IDs to delete |
| `page_id` | string | yes | Unbounce page ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedAt": "string",
      "createdAt": "string",
      "createdBy": "string",
      "id": "string",
      "metadata": {},
      "pageId": "string",
      "query": {},
      "status": "string",
      "totalLeadsDeleted": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedAt` | string | Completion timestamp from the example response. |
| `createdAt` | string | Creation timestamp from the Unbounce example response. |
| `createdBy` | string | Identifier of the user or system that created the deletion request. |
| `id` | string | Lead deletion request ID from the Unbounce example response. |
| `metadata` | object | Metadata object from the Unbounce example response. |
| `pageId` | string | Page ID associated with the lead deletion request. |
| `query` | object | Deletion query payload from the example response. |
| `status` | string | Current status of the lead deletion request. |
| `totalLeadsDeleted` | number | Total number of leads deleted by the request. |

## Native endpoint

Through the native Unbounce API, this operation is `POST /pages/:page_id/lead_deletion_request` (base URL `https://api.unbounce.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lead-deletion-request.md) for the provider-specific parameters and requirements.

