# Formstack: Update Submission

Updates an existing submission in Formstack.

```
PUT https://connect.mindcloud.co/v1/universal/formstack/latest/actions/update-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formstack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/formstack/latest/actions/update-submission" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "submissionId": 1,
  "fields[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formstack/latest/actions/update-submission', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "submissionId": 1,
    "fields[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `submissionId` | number | yes | The unique identifier of the submission to edit. |
| `fields[]` | array<object> | yes | Array of field values to update. |
| `fields[].id` | string | no | The ID of the field to update. |
| `fields[].value` | object | no | Provide the Formstack typed field-value object. For text fields use `{ "value": "example text" }`. |
| `read` | list<string> | no | Flag to mark the submission as read. One of: `false`, `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userAgent` | string | no | User agent of the submission. |
| `remoteAddr` | string | no | Remote address of the submission. |
| `paymentStatus` | string | no | Payment status of the submission. |
| `timestamp` | date | no | Timestamp of the submission. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "formId": 1,
      "id": 1,
      "paymentStatus": "string",
      "read": "string",
      "remoteAddr": "string",
      "timestamp": "2026-05-07T12:00:00.000Z",
      "userAgent": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `formId` | number | The ID of the form this submission belongs to. |
| `id` | number | The ID of the submission. |
| `paymentStatus` | string | Payment status of the submission. |
| `read` | string | Read status returned by the submission update response. |
| `remoteAddr` | string | Remote address of the submission. |
| `timestamp` | date | Timestamp of the submission. |
| `userAgent` | string | User agent of the submission. |

## Native endpoint

Through the native Formstack API, this operation is `PUT /submissions/:submissionId` (base URL `https://www.formstack.com/api/v2025`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-submission.md) for the provider-specific parameters and requirements.

