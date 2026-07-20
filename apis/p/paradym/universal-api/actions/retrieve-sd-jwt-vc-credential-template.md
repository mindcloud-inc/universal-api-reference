# Paradym: Retrieve Sd-Jwt Vc Credential Template

Retrieves an SD-JWT VC credential template from Paradym.

```
GET https://connect.mindcloud.co/v1/universal/paradym/latest/actions/retrieve-sd-jwt-vc-credential-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paradym `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paradym/latest/actions/retrieve-sd-jwt-vc-credential-template?connectionId=$CONNECTION_ID&credentialTemplateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "credentialTemplateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paradym/latest/actions/retrieve-sd-jwt-vc-credential-template?${params}`, {
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
| `credentialTemplateId` | string | yes | The SD-JWT VC credential template ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Paradym API returns.

## Native endpoint

Through the native Paradym API, this operation is `GET /projects/:projectId/templates/credentials/sd-jwt-vc/:credentialTemplateId` (base URL `https://api.paradym.id/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-sd-jwt-vc-credential-template.md) for the provider-specific parameters and requirements.

