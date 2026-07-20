# Informizely: List Responses



```
GET https://connect.mindcloud.co/v1/universal/informizely/latest/actions/list-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Informizely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/informizely/latest/actions/list-responses?connectionId=$CONNECTION_ID&surveyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/informizely/latest/actions/list-responses?${params}`, {
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
| `surveyId` | string | yes | The ID of the survey whose responses you want to retrieve. |
| `fromDate` | date | no | The earliest UTC timestamp to include, in ISO 8601 format. |
| `toDate` | date | no | The latest UTC timestamp to include, in ISO 8601 format. |
| `fromIndex` | number | no | The zero-based start index after any date filtering is applied. |
| `toIndex` | number | no | The zero-based end index after any date filtering is applied. |
| `includeRemoved` | boolean | no | Keep this true to include data for removed questions. Default: `true`. |
| `includeEmpty` | boolean | no | Keep this true to include empty answers. Default: `true`. |
| `excludeQuestions` | boolean | no | Set to true to omit question metadata from the response payload. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Questions": [
        {}
      ],
      "Responses": [
        {}
      ],
      "ResponseTags": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Questions` | array<object> | The question definitions included with the response payload. |
| `Responses` | array<object> | The survey responses returned by the request. |
| `ResponseTags` | array<object> | The response-tag definitions included with the response payload. |

## Native endpoint

Through the native Informizely API, this operation is `GET /responses` (base URL `https://api.informizely.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-responses.md) for the provider-specific parameters and requirements.

