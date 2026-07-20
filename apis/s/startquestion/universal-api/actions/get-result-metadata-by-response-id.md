# Startquestion: Get Result Metadata by Response ID

Retrieves survey results metadata from Startquestion by response ID.

```
GET https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/get-result-metadata-by-response-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Startquestion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/get-result-metadata-by-response-id?connectionId=$CONNECTION_ID&surveyId=1&responseId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "1",
  "responseId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/get-result-metadata-by-response-id?${params}`, {
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
| `responseId` | number | yes | Response ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {},
      "time": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta` | object | Result metadata. |
| `time` | object | Response timing metadata. |

## Native endpoint

Through the native Startquestion API, this operation is `GET /results/meta/:id_survey` (base URL `https://www.startquestion.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-result-metadata-by-response-id.md) for the provider-specific parameters and requirements.

