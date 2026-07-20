# Google Forms: List Form Responses

Retrieves form responses from Google Forms.

```
GET https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/list-form-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Forms `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/list-form-responses?connectionId=$CONNECTION_ID&limit=25&offset=0&formId=1FAIpQLSdExampleFormId" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "formId": "1FAIpQLSdExampleFormId"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/list-form-responses?${params}`, {
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
| `formId` | string | yes | The form identifier to list responses from. Example: `1FAIpQLSdExampleFormId`. |
| `submittedAfter` | string | no | Return responses submitted after this RFC3339 UTC timestamp, for example 2026-05-01T00:00:00Z. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `submittedAtOrAfter` | string | no | Return responses submitted at or after this RFC3339 UTC timestamp. |
| `filter` | string | no | Raw Google Forms response filter. Currently supports timestamp > N or timestamp >= N. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextPageToken": "string",
      "responses": [
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
| `nextPageToken` | string |  |
| `responses` | array<object> |  |

## Native endpoint

Through the native Google Forms API, this operation is `GET /:formId/responses` (base URL `https://forms.googleapis.com/v1/forms`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-form-responses.md) for the provider-specific parameters and requirements.

