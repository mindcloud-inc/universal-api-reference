# CustomJS: Execute Custom JavaScript

Executes custom JavaScript code in CustomJS.

```
GET https://connect.mindcloud.co/v1/universal/customJS/latest/actions/execute-custom-java-script
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomJS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customJS/latest/actions/execute-custom-java-script?connectionId=$CONNECTION_ID&code=string&input=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "code": "string",
  "input": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customJS/latest/actions/execute-custom-java-script?${params}`, {
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
| `code` | string | yes | JavaScript code to execute. |
| `input` | string | yes | Input payload made available to the JavaScript code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native CustomJS API, this operation is `POST https://e.customjs.io/__js1-` (base URL `https://e.customjs.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/execute-custom-java-script.md) for the provider-specific parameters and requirements.

