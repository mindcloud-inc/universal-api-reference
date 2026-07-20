# Startquestion: Get Result Metadata by Token

Retrieves survey results metadata from Startquestion by token.

```
GET https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/get-result-metadata-by-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Startquestion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/get-result-metadata-by-token?connectionId=$CONNECTION_ID&surveyId=1&token=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "1",
  "token": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/get-result-metadata-by-token?${params}`, {
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
| `token` | string | yes | Respondent token. |

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

Through the native Startquestion API, this operation is `GET /results/meta/:id_survey` (base URL `https://www.startquestion.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-result-metadata-by-token.md) for the provider-specific parameters and requirements.

