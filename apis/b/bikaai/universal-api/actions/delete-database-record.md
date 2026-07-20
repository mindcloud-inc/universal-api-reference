# Bika.ai: Delete Database Record

Deletes a database record from Bika.ai.

```
DELETE https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/delete-database-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bika.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/delete-database-record?connectionId=$CONNECTION_ID&spaceId=string&nodeId=string&recordId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "spaceId": "string",
  "nodeId": "string",
  "recordId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/delete-database-record?${params}`, {
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
| `spaceId` | string | yes | Bika.ai workspace/space ID. |
| `nodeId` | string | yes | Database node ID. In Bika.ai, the node ID is equivalent to the database ID for database resources. |
| `recordId` | string | yes | Record ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": true,
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data` | boolean |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Bika.ai API, this operation is `DELETE /spaces/:spaceId/resources/databases/:nodeId/records/:recordId` (base URL `https://bika.ai/api/openapi/bika/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-database-record.md) for the provider-specific parameters and requirements.

