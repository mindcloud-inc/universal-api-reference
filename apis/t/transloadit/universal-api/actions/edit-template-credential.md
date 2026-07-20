# Transloadit: Edit Template Credential

Updates an existing template credential in Transloadit.

```
PUT https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/edit-template-credential
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transloadit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/edit-template-credential" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "credentialsId": "string",
  "params": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/edit-template-credential', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "credentialsId": "string",
    "params": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `credentialsId` | string | yes | The ID or name of the template credential to edit. |
| `params` | string | yes | JSON string containing the updated Transloadit template credential definition. |

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
| `credential` | object | Updated template credential object. |
| `message` | string | Human-readable result message. |
| `ok` | string | Status code returned by Transloadit for template credential update. |

## Native endpoint

Through the native Transloadit API, this operation is `PUT /template_credentials/:credentialsId` (base URL `https://api2.transloadit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-template-credential.md) for the provider-specific parameters and requirements.

