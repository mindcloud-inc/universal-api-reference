# Cognito Forms: Get Import Status



```
GET https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/get-import-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cognito Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/get-import-status?connectionId=$CONNECTION_ID&formId=string&importId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string",
  "importId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/get-import-status?${params}`, {
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
| `formId` | string | yes |  |
| `importId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorMessage": "string",
      "id": "string",
      "importLink": "https://example.com",
      "status": "string",
      "successfulEntries": 1,
      "totalEntries": 1,
      "unsuccessfulEntries": 1
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
| `importLink` | string | Link to the annotated import results. |
| `status` | string | Current import status. |
| `successfulEntries` | number | Number of successfully imported entries. |
| `totalEntries` | number | Total number of entries in the import. |
| `unsuccessfulEntries` | number | Number of entries that failed to import. |

## Native endpoint

Through the native Cognito Forms API, this operation is `GET /forms/:formId/import-status/:importId` (base URL `https://www.cognitoforms.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-import-status.md) for the provider-specific parameters and requirements.

