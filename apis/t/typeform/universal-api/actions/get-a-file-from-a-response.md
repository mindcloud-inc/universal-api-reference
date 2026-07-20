# Typeform: Get a File from a Response



```
GET https://connect.mindcloud.co/v1/universal/typeform/latest/actions/get-a-file-from-a-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typeform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typeform/latest/actions/get-a-file-from-a-response?connectionId=$CONNECTION_ID&fieldId=string&filename=Ava%20Chen&formId=string&responseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fieldId": "string",
  "filename": "Ava Chen",
  "formId": "string",
  "responseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typeform/latest/actions/get-a-file-from-a-response?${params}`, {
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
| `fieldId` | string | yes | Typeform field identifier. |
| `filename` | string | yes | Uploaded file name. |
| `formId` | string | yes | Typeform form identifier. |
| `inline` | boolean | no | Return file inline instead of attachment. |
| `responseId` | string | yes | Typeform response identifier. |

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
| `value` | string | Binary download response for the requested file from a response. |

## Native endpoint

Through the native Typeform API, this operation is `GET /forms/:formId/responses/:responseId/fields/:fieldId/files/:filename` (base URL `https://api.typeform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-file-from-a-response.md) for the provider-specific parameters and requirements.

