# Cognito Forms: Import Entries Create New



```
POST https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/import-entries-create-new
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cognito Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/import-entries-create-new" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "entries": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/import-entries-create-new', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "entries": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes |  |
| `entries` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorMessage": "string",
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorMessage` | string | Error message when the import fails. |
| `id` | string | Import job ID. |
| `status` | string | Current import status. |

## Native endpoint

Through the native Cognito Forms API, this operation is `POST /forms/:formId/import-entries` (base URL `https://www.cognitoforms.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-entries-create-new.md) for the provider-specific parameters and requirements.

