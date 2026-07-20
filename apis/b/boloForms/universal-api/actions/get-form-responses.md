# BoloForms: Get Form Responses

Retrieves responses from a BoloForms form.

```
GET https://connect.mindcloud.co/v1/universal/boloForms/latest/actions/get-form-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BoloForms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boloForms/latest/actions/get-form-responses?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boloForms/latest/actions/get-form-responses?${params}`, {
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
| `formId` | string | yes | ID of the form to retrieve responses for |
| `page` | number | no | Page number for pagination |
| `limit` | number | no | Number of responses per page |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `responseId` | string | no | Specific response ID to retrieve |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answers": [
        {}
      ],
      "formId": "string",
      "responseId": "string",
      "submittedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answers` | array<object> | Submitted answers for the response. |
| `formId` | string | Form ID associated with the response. |
| `responseId` | string | Form response ID returned by BoloSign. |
| `submittedAt` | string | Submission timestamp for the response. |

## Native endpoint

Through the native BoloForms API, this operation is `GET /get-form-responses` (base URL `https://sapi.boloforms.com/signature`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-responses.md) for the provider-specific parameters and requirements.

