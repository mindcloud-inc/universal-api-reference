# Informizely: Get Response Count



```
GET https://connect.mindcloud.co/v1/universal/informizely/latest/actions/get-response-count
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Informizely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/informizely/latest/actions/get-response-count?connectionId=$CONNECTION_ID&surveyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/informizely/latest/actions/get-response-count?${params}`, {
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
| `surveyId` | string | yes | The ID of the survey whose response count you want to retrieve. |
| `fromDate` | date | no | The earliest UTC timestamp to include, in ISO 8601 format. |
| `toDate` | date | no | The latest UTC timestamp to include, in ISO 8601 format. |
| `fromIndex` | number | no | The zero-based start index after any date filtering is applied. |
| `toIndex` | number | no | The zero-based end index after any date filtering is applied. |
| `includeRemoved` | boolean | no | Keep this true to include data for removed questions. Default: `true`. |
| `includeEmpty` | boolean | no | Keep this true to include empty answers. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | number | The total number of survey responses returned by the count endpoint. |

## Native endpoint

Through the native Informizely API, this operation is `GET /count` (base URL `https://api.informizely.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-response-count.md) for the provider-specific parameters and requirements.

