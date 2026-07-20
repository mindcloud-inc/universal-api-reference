# Jotform: Create Form Submission

Creates a form submission in Jotform.

```
POST https://connect.mindcloud.co/v1/universal/jotform/latest/actions/create-form-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jotform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jotform/latest/actions/create-form-submission" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "submission": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jotform/latest/actions/create-form-submission', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "submission": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | Form ID |
| `submission` | object | yes | Submission payload keyed by question identifiers. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "submissionID": "string",
      "URL": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `submissionID` | string |  |
| `URL` | string |  |

## Native endpoint

Through the native Jotform API, this operation is `POST /form/:formId/submissions` (base URL `https://api.jotform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-form-submission.md) for the provider-specific parameters and requirements.

