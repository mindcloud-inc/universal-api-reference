# Cognito Forms: Delete Entry



```
DELETE https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/delete-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cognito Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/delete-entry?connectionId=$CONNECTION_ID&formId=string&entryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string",
  "entryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/delete-entry?${params}`, {
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
| `formId` | string | yes | The ID of the Form for which you want to delete an Entry |
| `entryId` | string | yes | The ID of the Entry you want to delete |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | Empty response body returned when the entry is deleted successfully. |

## Native endpoint

Through the native Cognito Forms API, this operation is `DELETE /forms/:formId/entries/:entryId` (base URL `https://www.cognitoforms.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-entry.md) for the provider-specific parameters and requirements.

