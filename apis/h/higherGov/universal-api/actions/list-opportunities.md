# HigherGov: List Opportunities

Retrieves government opportunities from HigherGov.

```
GET https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-opportunities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HigherGov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-opportunities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-opportunities?${params}`, {
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
| `agencyKey` | string | no | HigherGov Agency key |
| `capturedDate` | string | no | Date the opportunity was added to HigherGov |
| `oppKey` | string | no | HigherGov opportunity key |
| `postedDate` | string | no | Date the opportunity was posted in YYYY-MM-DD format |
| `searchId` | string | no | HigherGov SearchID |
| `sourceId` | string | no | Source opportunity ID |
| `sourceType` | string | no | Opportunity source type (sam, dibbs, sbir, grant, sled) |
| `versionKey` | string | no | HigherGov opportunity version key |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agency": {},
      "ai_summary": "string",
      "captured_date": "string",
      "description_text": "string",
      "document_path": "string",
      "due_date": "string",
      "opp_cat": "string",
      "opp_key": "string",
      "path": "string",
      "posted_date": "string",
      "source_id": "string",
      "source_type": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agency` | object |  |
| `ai_summary` | string |  |
| `captured_date` | string |  |
| `description_text` | string |  |
| `document_path` | string |  |
| `due_date` | string |  |
| `opp_cat` | string |  |
| `opp_key` | string |  |
| `path` | string |  |
| `posted_date` | string |  |
| `source_id` | string |  |
| `source_type` | string |  |
| `title` | string |  |

## Native endpoint

Through the native HigherGov API, this operation is `GET /api-external/opportunity/` (base URL `https://www.highergov.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-opportunities.md) for the provider-specific parameters and requirements.

