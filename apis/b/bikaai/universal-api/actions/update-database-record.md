# Bika.ai: Update Database Record

Updates a database record in Bika.ai.

```
PUT https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/update-database-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bika.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/update-database-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spaceId": "string",
  "nodeId": "string",
  "id": "string",
  "cells": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/update-database-record', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spaceId": "string",
    "nodeId": "string",
    "id": "string",
    "cells": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `spaceId` | string | yes | Bika.ai workspace/space ID. |
| `nodeId` | string | yes | Database node ID. In Bika.ai, the node ID is equivalent to the database ID for database resources. |
| `id` | string | yes | Record ID to update, sent in the request body as documented by Bika.ai. |
| `cells` | object | yes | Object whose keys are field names and values are the updated cell values. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "cells": {},
        "commentCount": 1,
        "databaseId": "string",
        "groupCount": 1,
        "id": "string",
        "revision": 1
      },
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
| `data` | object |  |
| `data.cells` | object |  |
| `data.commentCount` | number |  |
| `data.databaseId` | string |  |
| `data.groupCount` | number |  |
| `data.id` | string |  |
| `data.revision` | number |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Bika.ai API, this operation is `PATCH /spaces/:spaceId/resources/databases/:nodeId/records` (base URL `https://bika.ai/api/openapi/bika/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-database-record.md) for the provider-specific parameters and requirements.

