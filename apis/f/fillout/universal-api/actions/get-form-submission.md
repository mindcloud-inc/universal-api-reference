# Fillout: Get Form Submission

Retrieves a form submission from Fillout.

```
GET https://connect.mindcloud.co/v1/universal/fillout/latest/actions/get-form-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fillout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fillout/latest/actions/get-form-submission?connectionId=$CONNECTION_ID&formId=string&submissionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string",
  "submissionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fillout/latest/actions/get-form-submission?${params}`, {
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
| `formId` | string | yes | The public identifier of the form. |
| `submissionId` | string | yes | The identifier of the submission. |

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
| `submission` | object |  |

## Native endpoint

Through the native Fillout API, this operation is `GET /forms/:formId/submissions/:submissionId` (base URL `https://api.fillout.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-submission.md) for the provider-specific parameters and requirements.

