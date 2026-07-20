# Google Forms: Get Form Response

Retrieves a form response from Google Forms.

```
GET https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/get-form-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/get-form-response?connectionId=$CONNECTION_ID&formId=string&responseId=Ae4q2VsL..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string",
  "responseId": "Ae4q2VsL..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/get-form-response?${params}`, {
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
| `formId` | string | yes | The form identifier. |
| `responseId` | string | yes | The response identifier. Example: `Ae4q2VsL...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": "string",
      "error": {
        "code": "string",
        "message": "string"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details` | string |  |
| `error.code` | string |  |
| `error.message` | string |  |
| `message` | string |  |

## Native endpoint

Through the native Google Forms API, this operation is `GET /:formId/responses/:responseId` (base URL `https://forms.googleapis.com/v1/forms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-response.md) for the provider-specific parameters and requirements.

