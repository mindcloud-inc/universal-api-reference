# Paradym: List Mdoc Credential Templates

Retrieves mdoc credential templates from Paradym.

```
GET https://connect.mindcloud.co/v1/universal/paradym/latest/actions/list-mdoc-credential-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paradym `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paradym/latest/actions/list-mdoc-credential-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paradym/latest/actions/list-mdoc-credential-templates?${params}`, {
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
| `name` | string | no | Search templates by name. Example: `MindCloud Test Mdoc 20260402`. |
| `credentialType` | string | no | Filter templates by credential type. Example: `org.mindcloud.test.card`. |
| `archived` | boolean | no | Filter templates by archived state. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
      "meta": {
        "filter": {
          "archived": true
        },
        "page": {
          "maxSize": "string",
          "size": "string"
        },
        "search": {
          "name": "Ava Chen"
        },
        "sort": [
          {
            "id": "string"
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].archivedAt` | object |  |
| `data[].attributes.org.mindcloud.test.card.properties.fullName.description` | string |  |
| `data[].attributes.org.mindcloud.test.card.properties.fullName.name` | string |  |
| `data[].attributes.org.mindcloud.test.card.properties.fullName.required` | boolean |  |
| `data[].attributes.org.mindcloud.test.card.properties.fullName.type` | string |  |
| `data[].createdAt` | string |  |
| `data[].description` | string |  |
| `data[].format` | string |  |
| `data[].id` | string |  |
| `data[].issuer.keyType` | string |  |
| `data[].issuer.signer` | string |  |
| `data[].name` | string |  |
| `data[].type` | string |  |
| `data[].updatedAt` | string |  |
| `data[].validUntil.future.years` | number |  |
| `meta.filter.archived` | boolean |  |
| `meta.page.maxSize` | string |  |
| `meta.page.size` | string |  |
| `meta.search.name` | string |  |
| `meta.sort[].id` | string |  |

## Native endpoint

Through the native Paradym API, this operation is `GET /projects/:projectId/templates/credentials/mdoc` (base URL `https://api.paradym.id/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-mdoc-credential-templates.md) for the provider-specific parameters and requirements.

