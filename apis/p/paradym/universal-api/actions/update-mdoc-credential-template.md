# Paradym: Update Mdoc Credential Template

Updates an mdoc credential template in Paradym.

```
PUT https://connect.mindcloud.co/v1/universal/paradym/latest/actions/update-mdoc-credential-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paradym `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/paradym/latest/actions/update-mdoc-credential-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "credentialTemplateId": "string",
  "name": "Ava Chen",
  "validUntil.future.years": 1,
  "attributes": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paradym/latest/actions/update-mdoc-credential-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "credentialTemplateId": "string",
    "name": "Ava Chen",
    "validUntil.future.years": 1,
    "attributes": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `credentialTemplateId` | string | yes | Template to update. |
| `name` | string | yes | Template name. |
| `description` | string | no | Optional template description. Example: `Updated runtime test template`. |
| `validUntil.future.years` | number | yes | Number of years after issuance that the credential remains valid. |
| `attributes` | object | yes | Attributes schema object keyed by credential namespace. Example: {"org.mindcloud.test.card":{"properties":{"fullName":{"type":"string","name":"Full Name","required":true}}}} |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Paradym API returns.

## Native endpoint

Through the native Paradym API, this operation is `PUT /projects/:projectId/templates/credentials/mdoc/:credentialTemplateId` (base URL `https://api.paradym.id/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-mdoc-credential-template.md) for the provider-specific parameters and requirements.

