# Form.io: Update Form Submission

Updates an existing form submission in your Form.io project.

```
PUT https://connect.mindcloud.co/v1/universal/formio/latest/actions/update-form-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Form.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/formio/latest/actions/update-form-submission" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {},
  "formId": "string",
  "submissionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formio/latest/actions/update-form-submission', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": {},
    "formId": "string",
    "submissionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | yes | Updated submission data object keyed by component API keys. |
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

Through the native Form.io API, this operation is `PUT /form/:formId/submission/:submissionId` (base URL `https://neabnzbnvbushtk.form.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-form-submission.md) for the provider-specific parameters and requirements.

