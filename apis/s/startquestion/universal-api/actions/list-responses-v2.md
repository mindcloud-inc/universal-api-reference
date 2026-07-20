# Startquestion: List Responses V2

Retrieves survey responses from Startquestion with the v2 results format.

```
GET https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/list-responses-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Startquestion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/list-responses-v2?connectionId=$CONNECTION_ID&surveyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/list-responses-v2?${params}`, {
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
| `page` | number | no | Page number. |
| `limit` | number | no | Rows per page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {},
      "questions": [
        {}
      ],
      "time": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta` | object | Response metadata. |
| `questions` | array<object> | Answered questions. |
| `time` | object | Response duration metadata. |

## Native endpoint

Through the native Startquestion API, this operation is `GET /results/single-sheets/:id_survey` (base URL `https://www.startquestion.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-responses-v2.md) for the provider-specific parameters and requirements.

