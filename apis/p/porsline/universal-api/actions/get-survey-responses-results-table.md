# Porsline: Get Survey Responses Results Table



```
GET https://connect.mindcloud.co/v1/universal/porsline/latest/actions/get-survey-responses-results-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Porsline `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/porsline/latest/actions/get-survey-responses-results-table?connectionId=$CONNECTION_ID&survey_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "survey_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/porsline/latest/actions/get-survey-responses-results-table?${params}`, {
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
| `survey_id` | number | yes | The id of the target survey. |
| `since` | string | no | Limit submitted responders since the specified ISO 8601 datetime. |
| `until` | string | no | Limit submitted responders until the specified ISO 8601 datetime. |
| `sort` | string | no | Sort criteria in the Porsline {col_type},{object_id},{asc\|desc} format. |
| `page` | number | no | Page number. |
| `pageSize` | number | no | Maximum number of responders to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": [
        "string"
      ],
      "header": [
        "string"
      ],
      "invisibleRespondersCount": 1,
      "respondersCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | array | Results-table row data. |
| `header` | array | Results-table column metadata. |
| `invisibleRespondersCount` | number | Total invisible responders. |
| `respondersCount` | number | Total visible responders. |

## Native endpoint

Through the native Porsline API, this operation is `GET /api/v2/surveys/:survey_id/responses/results-table/` (base URL `https://survey.porsline.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-survey-responses-results-table.md) for the provider-specific parameters and requirements.

