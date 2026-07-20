# Fillout Forms: Create Submissions

Creates submissions for a Fillout form.

```
POST https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/create-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fillout Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/create-submissions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "submissions[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/create-submissions', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "submissions[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | The form ID to create submissions for. |
| `submissions[]` | array<object> | yes | The list of submissions to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "submissions": [
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
| `submissions` | array<object> | Created submission records. |

## Native endpoint

Through the native Fillout Forms API, this operation is `POST /forms/:formId/submissions` (base URL `https://api.fillout.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-submissions.md) for the provider-specific parameters and requirements.

