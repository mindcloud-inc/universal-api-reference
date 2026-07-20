# Fillout Forms: Get Submission by ID

Retrieves a submission by ID from Fillout.

```
GET https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/get-submission-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fillout Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/get-submission-by-id?connectionId=$CONNECTION_ID&formId=string&submissionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string",
  "submissionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/get-submission-by-id?${params}`, {
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
| `formId` | string | yes | The form ID that owns the submission. |
| `submissionId` | string | yes | The submission ID to retrieve. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeEditLink` | boolean | no | Whether to include an edit link in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "submission": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `submission` | object | Submission details for the requested submission. |

## Native endpoint

Through the native Fillout Forms API, this operation is `GET /forms/:formId/submissions/:submissionId` (base URL `https://api.fillout.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-submission-by-id.md) for the provider-specific parameters and requirements.

