# Paradym: Retrieve Mdoc Credential Template

Retrieves an mdoc credential template from Paradym.

```
GET https://connect.mindcloud.co/v1/universal/paradym/latest/actions/retrieve-mdoc-credential-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paradym `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paradym/latest/actions/retrieve-mdoc-credential-template?connectionId=$CONNECTION_ID&credentialTemplateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "credentialTemplateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paradym/latest/actions/retrieve-mdoc-credential-template?${params}`, {
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
| `credentialTemplateId` | string | yes | Template to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archivedAt": {},
      "attributes": {
        "org": {
          "mindcloud": {
            "test": {
              "card": {
                "properties": {
                  "fullName": {
                    "description": "Ava Chen",
                    "name": "Ava Chen",
                    "required": true,
                    "type": "Ava Chen"
                  }
                }
              }
            }
          }
        }
      },
      "createdAt": "string",
      "description": "string",
      "format": "string",
      "id": "string",
      "issuer": {
        "keyType": "string",
        "signer": "string"
      },
      "name": "Ava Chen",
      "type": "string",
      "updatedAt": "string",
      "validUntil": {
        "future": {
          "years": 1
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archivedAt` | object |  |
| `attributes.org.mindcloud.test.card.properties.fullName.description` | string |  |
| `attributes.org.mindcloud.test.card.properties.fullName.name` | string |  |
| `attributes.org.mindcloud.test.card.properties.fullName.required` | boolean |  |
| `attributes.org.mindcloud.test.card.properties.fullName.type` | string |  |
| `createdAt` | string |  |
| `description` | string |  |
| `format` | string |  |
| `id` | string |  |
| `issuer.keyType` | string |  |
| `issuer.signer` | string |  |
| `name` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |
| `validUntil.future.years` | number |  |

## Native endpoint

Through the native Paradym API, this operation is `GET /projects/:projectId/templates/credentials/mdoc/:credentialTemplateId` (base URL `https://api.paradym.id/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-mdoc-credential-template.md) for the provider-specific parameters and requirements.

