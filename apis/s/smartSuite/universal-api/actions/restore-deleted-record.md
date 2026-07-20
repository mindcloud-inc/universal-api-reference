# SmartSuite: Restore Deleted Record

Restores a deleted record in SmartSuite.

```
PUT https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/restore-deleted-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/restore-deleted-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recordId": "69b852a3ca174ae462dcc9eb"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/restore-deleted-record', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "recordId": "69b852a3ca174ae462dcc9eb"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recordId` | string | yes | The deleted SmartSuite record ID from the deleted-records API. SmartSuite documents this path token as record_id. Example: `69b852a3ca174ae462dcc9eb`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountSlug": "string",
      "applicationId": "string",
      "applicationName": "Ava Chen",
      "applicationRecordTerm": "string",
      "autonumber": 1,
      "deletedBy": "string",
      "deletedDate": {
        "date": "string",
        "includeTime": true
      },
      "description": "string",
      "firstCreated": {
        "by": "string",
        "on": "string"
      },
      "formId": {},
      "id": "string",
      "isDemo": true,
      "lastUpdated": {
        "by": "string",
        "on": "string"
      },
      "ranking": {
        "default": "string"
      },
      "s1a2bf428a": "string",
      "sa6bf27e4f": "string",
      "solutionId": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountSlug` | string |  |
| `applicationId` | string |  |
| `applicationName` | string |  |
| `applicationRecordTerm` | string |  |
| `autonumber` | number |  |
| `deletedBy` | string |  |
| `deletedDate.date` | string |  |
| `deletedDate.includeTime` | boolean |  |
| `description` | string |  |
| `firstCreated.by` | string |  |
| `firstCreated.on` | string |  |
| `formId` | object |  |
| `id` | string |  |
| `isDemo` | boolean |  |
| `lastUpdated.by` | string |  |
| `lastUpdated.on` | string |  |
| `ranking.default` | string |  |
| `s1a2bf428a` | string |  |
| `sa6bf27e4f` | string |  |
| `solutionId` | string |  |
| `title` | string |  |

## Native endpoint

Through the native SmartSuite API, this operation is `POST /deleted-records/:recordId/restore/` (base URL `https://app.smartsuite.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/restore-deleted-record.md) for the provider-specific parameters and requirements.

