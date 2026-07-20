# Startquestion: Download Result Attachment

Downloads a survey response attachment from Startquestion.

```
GET https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/download-result-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Startquestion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/download-result-attachment?connectionId=$CONNECTION_ID&surveyId=1&fillId=1&questionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "1",
  "fillId": "1",
  "questionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/download-result-attachment?${params}`, {
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
| `surveyId` | number | yes | Survey ID. |
| `fillId` | number | yes | Fill ID. |
| `questionId` | number | yes | Attachment question ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "file": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `file` | string | Attachment file payload. |

## Native endpoint

Through the native Startquestion API, this operation is `GET https://app.startquestion.com/api/v2/results/:surveyId/fill/:fillId/attachment/:questionId` (base URL `https://www.startquestion.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-result-attachment.md) for the provider-specific parameters and requirements.

