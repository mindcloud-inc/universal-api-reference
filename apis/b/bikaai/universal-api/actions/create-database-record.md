# Bika.ai: Create Database Record

Creates a database record in Bika.ai.

```
POST https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/create-database-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bika.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/create-database-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spaceId": "string",
  "nodeId": "string",
  "cells": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/create-database-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spaceId": "string",
    "nodeId": "string",
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
| `cells` | object | yes | Object whose keys are field names and values are the cell values to write. |

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

Through the native Bika.ai API, this operation is `POST /spaces/:spaceId/resources/databases/:nodeId/records` (base URL `https://bika.ai/api/openapi/bika/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-database-record.md) for the provider-specific parameters and requirements.

