# SmartSuite: List Deleted Records

Retrieves deleted records from SmartSuite.

```
GET https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/list-deleted-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/list-deleted-records?connectionId=$CONNECTION_ID&solutionId=69b45da87cb40fc74dbb4b83" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "solutionId": "69b45da87cb40fc74dbb4b83"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/list-deleted-records?${params}`, {
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
| `solutionId` | string | yes | The SmartSuite solution ID whose deleted records should be listed. Example: `69b45da87cb40fc74dbb4b83`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applicationId": "string",
      "applicationName": "Ava Chen",
      "applicationRecordTerm": "string",
      "applicationSlug": "string",
      "deletedBy": "string",
      "deletedDate": {
        "date": "string",
        "includeTime": true
      },
      "id": "string",
      "lastUpdated": {
        "by": "string",
        "on": "string"
      },
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
| `applicationId` | string |  |
| `applicationName` | string |  |
| `applicationRecordTerm` | string |  |
| `applicationSlug` | string |  |
| `deletedBy` | string |  |
| `deletedDate.date` | string |  |
| `deletedDate.includeTime` | boolean |  |
| `id` | string |  |
| `lastUpdated.by` | string |  |
| `lastUpdated.on` | string |  |
| `solutionId` | string |  |
| `title` | string |  |

## Native endpoint

Through the native SmartSuite API, this operation is `POST /deleted-records/` (base URL `https://app.smartsuite.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deleted-records.md) for the provider-specific parameters and requirements.

