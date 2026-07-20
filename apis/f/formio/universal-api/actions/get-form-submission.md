# Form.io: Get Form Submission

Retrieves a form submission from your Form.io project.

```
GET https://connect.mindcloud.co/v1/universal/formio/latest/actions/get-form-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Form.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formio/latest/actions/get-form-submission?connectionId=$CONNECTION_ID&formId=string&submissionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string",
  "submissionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formio/latest/actions/get-form-submission?${params}`, {
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
| `formId` | string | yes | The form ID containing the submission. |
| `submissionId` | string | yes | The submission ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "created": "string",
      "data": {},
      "form": "string",
      "modified": "string",
      "owner": "string",
      "project": "string",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `created` | string |  |
| `data` | object |  |
| `form` | string |  |
| `modified` | string |  |
| `owner` | string |  |
| `project` | string |  |
| `state` | string |  |

## Native endpoint

Through the native Form.io API, this operation is `GET /form/:formId/submission/:submissionId` (base URL `https://neabnzbnvbushtk.form.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-submission.md) for the provider-specific parameters and requirements.

