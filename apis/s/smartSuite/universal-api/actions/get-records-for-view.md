# SmartSuite: Get Records For View

Retrieves records for a SmartSuite view.

```
GET https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/get-records-for-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/get-records-for-view?connectionId=$CONNECTION_ID&tableId=69b45da87cb40fc74dbb4b84&reportId=69b8566f4b65a25e13c14c9d" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tableId": "69b45da87cb40fc74dbb4b84",
  "reportId": "69b8566f4b65a25e13c14c9d"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/get-records-for-view?${params}`, {
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
| `tableId` | string | yes | The SmartSuite table ID that owns the view. Example: `69b45da87cb40fc74dbb4b84`. |
| `reportId` | string | yes | The SmartSuite report or view ID to read records from. Example: `69b8566f4b65a25e13c14c9d`. |
| `withEmptyValues` | boolean | no | Whether SmartSuite should include empty field values in the record payload. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fields": [
        "string"
      ],
      "filter": {
        "operator": "string"
      },
      "records": [
        {
          "applicationId": "string",
          "applicationSlug": "string",
          "autonumber": 1,
          "commentsCount": 1,
          "firstCreated": {
            "by": "string",
            "on": "string"
          },
          "id": "string",
          "isDemo": true,
          "lastUpdated": {
            "by": "string",
            "on": "string"
          },
          "ranking": {
            "default": "string"
          },
          "title": "string"
        }
      ],
      "totalRecordsCount": 1,
      "unfiltered": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields[]` | string |  |
| `filter.operator` | string |  |
| `records[].applicationId` | string |  |
| `records[].applicationSlug` | string |  |
| `records[].autonumber` | number |  |
| `records[].commentsCount` | number |  |
| `records[].firstCreated.by` | string |  |
| `records[].firstCreated.on` | string |  |
| `records[].id` | string |  |
| `records[].isDemo` | boolean |  |
| `records[].lastUpdated.by` | string |  |
| `records[].lastUpdated.on` | string |  |
| `records[].ranking.default` | string |  |
| `records[].title` | string |  |
| `totalRecordsCount` | number |  |
| `unfiltered` | boolean |  |

## Native endpoint

Through the native SmartSuite API, this operation is `GET /applications/:tableId/records-for-report/` (base URL `https://app.smartsuite.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-records-for-view.md) for the provider-specific parameters and requirements.

