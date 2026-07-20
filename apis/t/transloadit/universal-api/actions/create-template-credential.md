# Transloadit: Create Template Credential

Creates a new template credential in Transloadit.

```
POST https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/create-template-credential
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transloadit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/create-template-credential" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "params": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/create-template-credential', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "params": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `params` | string | yes | JSON string containing the Transloadit template credential definition. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credential": {},
      "message": "string",
      "ok": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credential` | object | Created template credential object. |
| `message` | string | Human-readable result message. |
| `ok` | string | Status code returned by Transloadit for template credential creation. |

## Native endpoint

Through the native Transloadit API, this operation is `POST /template_credentials` (base URL `https://api2.transloadit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template-credential.md) for the provider-specific parameters and requirements.

