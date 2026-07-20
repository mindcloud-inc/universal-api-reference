# Survicate: Get Response

Retrieves a specific survey response from Survicate.

```
GET https://connect.mindcloud.co/v1/universal/survicate/latest/actions/get-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Survicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/survicate/latest/actions/get-response?connectionId=$CONNECTION_ID&surveyId=string&responseUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "string",
  "responseUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/survicate/latest/actions/get-response?${params}`, {
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
| `surveyId` | string | yes | The unique identifier of the survey containing the response. |
| `responseUuid` | string | yes | The unique UUID of the response to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answers": [
        {}
      ],
      "collectedAt": "2026-05-07T12:00:00.000Z",
      "deviceType": "string",
      "language": "string",
      "operatingSystem": "string",
      "platform": "string",
      "respondent": {
        "attributes": [
          {}
        ],
        "uuid": "string"
      },
      "url": "https://example.com",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answers` | array<object> | Answers submitted in the response. |
| `collectedAt` | date | Timestamp when the response was collected. |
| `deviceType` | string | Type of device used by the respondent. |
| `language` | string | Language shown to the respondent. |
| `operatingSystem` | string | Operating system used by the respondent. |
| `platform` | string | Client platform reported by Survicate. |
| `respondent.attributes` | array<object> | Respondent attributes included with the response. |
| `respondent.uuid` | string | Unique identifier of the respondent. |
| `url` | string | URL where the survey was displayed. |
| `uuid` | string | Unique identifier of the response. |

## Native endpoint

Through the native Survicate API, this operation is `GET /surveys/:survey_id/responses/:response_uuid` (base URL `https://data-api.survicate.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-response.md) for the provider-specific parameters and requirements.

