# Paradym: Retrieve Mdoc Credential Template JSON Schema

Retrieves an mdoc credential template JSON schema from Paradym.

```
GET https://connect.mindcloud.co/v1/universal/paradym/latest/actions/retrieve-mdoc-credential-template-json-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paradym `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paradym/latest/actions/retrieve-mdoc-credential-template-json-schema?connectionId=$CONNECTION_ID&credentialTemplateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "credentialTemplateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paradym/latest/actions/retrieve-mdoc-credential-template-json-schema?${params}`, {
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
| `credentialTemplateId` | string | yes | Template to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$id": "string",
      "$schema": "string",
      "additionalProperties": true,
      "description": "string",
      "properties": {
        "org": {
          "mindcloud": {
            "test": {
              "card": {
                "additionalProperties": true,
                "properties": {
                  "fullName": {
                    "description": "Ava Chen",
                    "title": "Ava Chen",
                    "type": "Ava Chen"
                  }
                },
                "required": [
                  "string"
                ],
                "type": "string"
              }
            }
          }
        }
      },
      "required": [
        "string"
      ],
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$id` | string |  |
| `$schema` | string |  |
| `additionalProperties` | boolean |  |
| `description` | string |  |
| `properties.org.mindcloud.test.card.additionalProperties` | boolean |  |
| `properties.org.mindcloud.test.card.properties.fullName.description` | string |  |
| `properties.org.mindcloud.test.card.properties.fullName.title` | string |  |
| `properties.org.mindcloud.test.card.properties.fullName.type` | string |  |
| `properties.org.mindcloud.test.card.required[]` | string |  |
| `properties.org.mindcloud.test.card.type` | string |  |
| `required[]` | string |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Paradym API, this operation is `GET /projects/:projectId/templates/credentials/mdoc/:credentialTemplateId/json-schema` (base URL `https://api.paradym.id/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-mdoc-credential-template-json-schema.md) for the provider-specific parameters and requirements.

