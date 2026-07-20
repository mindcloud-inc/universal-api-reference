# SmartSuite: Delete Record

Deletes an existing record from SmartSuite.

```
DELETE https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/delete-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/delete-record?connectionId=$CONNECTION_ID&tableId=69b8530e9d8596f0c0a03533&recordId=69b854140283883904ca54a0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tableId": "69b8530e9d8596f0c0a03533",
  "recordId": "69b854140283883904ca54a0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/delete-record?${params}`, {
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
| `tableId` | string | yes | The SmartSuite table ID that owns the record. Example: `69b8530e9d8596f0c0a03533`. |
| `recordId` | string | yes | The SmartSuite record ID to delete. Example: `69b854140283883904ca54a0`. |

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
      "deletedBy": "string",
      "deletedDate": {
        "date": "string",
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
| `deletedBy` | string |  |
| `deletedDate.date` | string |  |
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

Through the native SmartSuite API, this operation is `DELETE /applications/:table_id/records/:record_id/` (base URL `https://app.smartsuite.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-record.md) for the provider-specific parameters and requirements.

