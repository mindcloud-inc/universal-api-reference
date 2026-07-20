# SmartSuite: Create Record

Creates a new record in SmartSuite.

```
POST https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/create-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/create-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tableId": "69b8530e9d8596f0c0a03533",
  "record": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/create-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tableId": "69b8530e9d8596f0c0a03533",
    "record": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tableId` | string | yes | The SmartSuite table ID that will receive the new record. Example: `69b8530e9d8596f0c0a03533`. |
| `record` | object | yes | The SmartSuite record payload keyed by field slug. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applicationId": "string",
      "applicationSlug": "string",
      "autonumber": 1,
      "commentsCount": 1,
      "deletedBy": {},
      "deletedDate": {
        "date": {},
        "includeTime": true
      },
      "description": {
        "data": {
          "type": "string"
        },
        "html": "string",
        "preview": "string"
      },
      "dueDate": {
        "fromDate": {
          "date": {},
          "includeTime": true
        },
        "statusIsCompleted": true,
        "statusUpdatedOn": {},
        "toDate": {
          "date": {},
          "includeTime": true
        }
      },
      "firstCreated": {
        "by": "string",
        "on": "string"
      },
      "id": "string",
      "lastUpdated": {
        "by": "string",
        "on": "string"
      },
      "mctestfld1": "string",
      "priority": "string",
      "ranking": {
        "default": "string"
      },
      "status": {
        "updatedOn": "string",
        "value": "string"
      },
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicationId` | string |  |
| `applicationSlug` | string |  |
| `autonumber` | number |  |
| `commentsCount` | number |  |
| `deletedBy` | object |  |
| `deletedDate.date` | object |  |
| `deletedDate.includeTime` | boolean |  |
| `description.data.type` | string |  |
| `description.html` | string |  |
| `description.preview` | string |  |
| `dueDate.fromDate.date` | object |  |
| `dueDate.fromDate.includeTime` | boolean |  |
| `dueDate.statusIsCompleted` | boolean |  |
| `dueDate.statusUpdatedOn` | object |  |
| `dueDate.toDate.date` | object |  |
| `dueDate.toDate.includeTime` | boolean |  |
| `firstCreated.by` | string |  |
| `firstCreated.on` | string |  |
| `id` | string |  |
| `lastUpdated.by` | string |  |
| `lastUpdated.on` | string |  |
| `mctestfld1` | string |  |
| `priority` | string |  |
| `ranking.default` | string |  |
| `status.updatedOn` | string |  |
| `status.value` | string |  |
| `title` | string |  |

## Native endpoint

Through the native SmartSuite API, this operation is `POST /applications/:table_id/records/` (base URL `https://app.smartsuite.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-record.md) for the provider-specific parameters and requirements.

