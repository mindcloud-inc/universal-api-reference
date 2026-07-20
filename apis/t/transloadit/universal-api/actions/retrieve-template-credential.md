# Transloadit: Retrieve Template Credential

Retrieves a template credential from Transloadit.

```
GET https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/retrieve-template-credential
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transloadit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/retrieve-template-credential?connectionId=$CONNECTION_ID&credentialsId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "credentialsId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/retrieve-template-credential?${params}`, {
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
| `credentialsId` | string | yes | The ID or name of the template credential to retrieve. |

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
| `credential` | object | Retrieved template credential object. |
| `message` | string | Human-readable result message. |
| `ok` | string | Status code returned by Transloadit for template credential retrieval. |

## Native endpoint

Through the native Transloadit API, this operation is `GET /template_credentials/:credentialsId` (base URL `https://api2.transloadit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-template-credential.md) for the provider-specific parameters and requirements.

