# Didit: Delete Questionnaire

Deletes a questionnaire from Didit.

```
DELETE https://connect.mindcloud.co/v1/universal/didit/latest/actions/delete-questionnaire
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Didit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/didit/latest/actions/delete-questionnaire?connectionId=$CONNECTION_ID&questionnaireId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "questionnaireId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/didit/latest/actions/delete-questionnaire?${params}`, {
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
| `questionnaireId` | string | yes | Didit questionnaire identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Didit API returns.

## Native endpoint

Through the native Didit API, this operation is `DELETE /questionnaires/{questionnaireId}/` (base URL `https://verification.didit.me/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-questionnaire.md) for the provider-specific parameters and requirements.

