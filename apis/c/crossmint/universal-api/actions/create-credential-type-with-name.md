# Crossmint: Create Credential Type with Name

Creates a credential type with a name in Crossmint.

```
POST https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/create-credential-type-with-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crossmint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/create-credential-type-with-name" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "typeName": "CourseCompletionCertificate",
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "title": "Course completion",
  "type": "object",
  "properties": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/create-credential-type-with-name', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "typeName": "CourseCompletionCertificate",
    "$schema": "https://json-schema.org/draft/2020-12/schema",
    "title": "Course completion",
    "type": "object",
    "properties": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `typeName` | string | yes | The name of the credential type. Example: `CourseCompletionCertificate`. |
| `$schema` | string | yes | JSON Schema draft URL. Crossmint documents `https://json-schema.org/draft/2020-12/schema`. Default: `https://json-schema.org/draft/2020-12/schema`. |
| `title` | string | yes | Credential type title. Example: `Course completion`. |
| `description` | string | no | Credential type description. Example: `Describes the course completed and the assigned grade`. |
| `type` | string | yes | Top-level JSON Schema type. The docs example uses `object`. Default: `object`. |
| `properties` | object | yes | Credential schema properties object. Include at least a `credentialSubject` object definition. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "typeSchema": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Credential type identifier returned by Crossmint. |
| `typeSchema` | object | JSON schema payload for the created credential type. |

## Native endpoint

Through the native Crossmint API, this operation is `PUT /v1-alpha1/credentials/types/:typeName` (base URL `https://staging.crossmint.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-credential-type-with-name.md) for the provider-specific parameters and requirements.

