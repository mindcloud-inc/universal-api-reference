# Global Patron: Delete Form Submission Webhook

Deletes a form submission webhook from Global Patron.

```
DELETE https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/delete-form-submission-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Patron `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/delete-form-submission-webhook?connectionId=$CONNECTION_ID&formId=string&submissionWebhookId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string",
  "submissionWebhookId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/delete-form-submission-webhook?${params}`, {
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
| `formId` | string | yes | ID of the form. |
| `submissionWebhookId` | string | yes | ID of the submission webhook to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionSuccessful": true,
      "error": "string",
      "id": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionSuccessful` | boolean | Whether GlobalPatron reports the action was successful. |
| `error` | string | Provider error message when present. |
| `id` | string | Deleted webhook identifier. |
| `message` | string | Provider status message. |

## Native endpoint

Through the native Global Patron API, this operation is `DELETE /api/restricted/form/{formId}/submissionwebhook/{submissionWebhookId}` (base URL `https://api.globalpatron.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-form-submission-webhook.md) for the provider-specific parameters and requirements.

