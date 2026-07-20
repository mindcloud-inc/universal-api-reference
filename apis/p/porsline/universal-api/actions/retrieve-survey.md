# Porsline: Retrieve Survey



```
GET https://connect.mindcloud.co/v1/universal/porsline/latest/actions/retrieve-survey
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Porsline `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/porsline/latest/actions/retrieve-survey?connectionId=$CONNECTION_ID&survey_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "survey_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/porsline/latest/actions/retrieve-survey?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "closed": true,
      "labels": [
        "string"
      ],
      "language": "string",
      "name": "Ava Chen",
      "previewCode": "string",
      "reportCode": "string",
      "submittedResponses": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the survey is active. |
| `closed` | boolean | Whether the survey is closed. |
| `labels` | array<string> | Survey labels. |
| `language` | string | Survey language. |
| `name` | string | Survey name. |
| `previewCode` | string | Preview code. |
| `reportCode` | string | Report code. |
| `submittedResponses` | number | Submitted response count. |

## Native endpoint

Through the native Porsline API, this operation is `GET /api/v2/surveys/:survey_id/` (base URL `https://survey.porsline.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-survey.md) for the provider-specific parameters and requirements.

