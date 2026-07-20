# SmartSurvey: List Surveys

Retrieves all surveys in your SmartSurvey account.

```
GET https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/list-surveys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSurvey `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/list-surveys?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/list-surveys?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "date_created": "2026-05-07T12:00:00.000Z",
      "date_modified": "2026-05-07T12:00:00.000Z",
      "href": "string",
      "href_links": "https://example.com",
      "href_responses": "string",
      "id": 1,
      "nickname": "Ava Chen",
      "responses": 1,
      "status": "string",
      "survey_url": "https://example.com",
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date_created` | date |  |
| `date_modified` | date |  |
| `href` | string |  |
| `href_links` | string |  |
| `href_responses` | string |  |
| `id` | number |  |
| `nickname` | string |  |
| `responses` | number |  |
| `status` | string |  |
| `survey_url` | string |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native SmartSurvey API, this operation is `GET /surveys` (base URL `https://api.smartsurvey.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-surveys.md) for the provider-specific parameters and requirements.

