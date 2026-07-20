# OpnForm: Update Submission

Updates an existing submission in OpnForm.

```
PUT https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/update-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpnForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/update-submission" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "submissionId": 1,
  "fieldValues": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/update-submission', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "submissionId": 1,
    "fieldValues": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The numeric ID of the form that owns the submission. |
| `submissionId` | number | yes | The numeric ID of the submission to update. |
| `fieldValues` | object | yes | Object mapping OpnForm field IDs to the updated values for this submission. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `message` | string |  |
| `type` | string |  |

## Native endpoint

Through the native OpnForm API, this operation is `PUT /open/forms/:id/submissions/:submissionId` (base URL `https://api.opnform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-submission.md) for the provider-specific parameters and requirements.

