# Porsline: Get Survey Responses Export



```
GET https://connect.mindcloud.co/v1/universal/porsline/latest/actions/get-survey-responses-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Porsline `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/porsline/latest/actions/get-survey-responses-export?connectionId=$CONNECTION_ID&survey_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "survey_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/porsline/latest/actions/get-survey-responses-export?${params}`, {
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
| `exportFormat` | string | no | Export format. 1: xlsx, 2: csv. |
| `since` | string | no | Limit submitted responders since the specified ISO 8601 datetime. |
| `until` | string | no | Limit submitted responders until the specified ISO 8601 datetime. |
| `sort` | string | no | Sort criteria in the Porsline {col_type},{object_id},{asc\|desc} format. |
| `filter` | number | no | Filter ID to apply on results. |
| `inlineFilter` | string | no | Inline filter expression in the Porsline documented format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | CSV export content returned by Porsline. |

## Native endpoint

Through the native Porsline API, this operation is `GET /api/v2/surveys/:survey_id/responses/export/` (base URL `https://survey.porsline.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-survey-responses-export.md) for the provider-specific parameters and requirements.

