# Rowform: Get Form Responses

Retrieves form responses from Rowform.

```
GET https://connect.mindcloud.co/v1/universal/rowform/latest/actions/get-form-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rowform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rowform/latest/actions/get-form-responses?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rowform/latest/actions/get-form-responses?${params}`, {
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
| `formId` | string | yes | The Rowform form id to fetch responses for. |
| `limit` | number | no | Maximum number of responses to return. Rowform defaults to 25 and allows up to 100. Default: `25`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answers": [
        {}
      ],
      "form_id": "string",
      "form_title": "string",
      "id": "string",
      "raw_answers": {},
      "respondent_email": "ava@example.com",
      "submitted_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answers` | array<object> |  |
| `form_id` | string |  |
| `form_title` | string |  |
| `id` | string |  |
| `raw_answers` | object |  |
| `respondent_email` | string |  |
| `submitted_at` | date |  |

## Native endpoint

Through the native Rowform API, this operation is `GET /api/zapier/responses` (base URL `https://app.rowform.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-responses.md) for the provider-specific parameters and requirements.

