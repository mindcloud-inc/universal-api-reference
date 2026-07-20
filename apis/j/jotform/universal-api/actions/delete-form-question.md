# Jotform: Delete Form Question

Deletes an existing form question from Jotform.

```
DELETE https://connect.mindcloud.co/v1/universal/jotform/latest/actions/delete-form-question
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jotform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/jotform/latest/actions/delete-form-question?connectionId=$CONNECTION_ID&formId=string&questionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string",
  "questionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jotform/latest/actions/delete-form-question?${params}`, {
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
| `formId` | string | yes | Form ID |
| `questionId` | string | yes | Question ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider response message. |

## Native endpoint

Through the native Jotform API, this operation is `DELETE /form/:formId/question/:questionId` (base URL `https://api.jotform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-form-question.md) for the provider-specific parameters and requirements.

