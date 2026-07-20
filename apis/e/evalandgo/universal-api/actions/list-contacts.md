# Evalandgo: List Contacts

Retrieves contacts from Evalandgo.

```
GET https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evalandgo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/list-contacts?${params}`, {
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
| `email` | string | no |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `username` | string | no |  |
| `phone` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@context": "string",
      "@id": "string",
      "@type": "string",
      "hydra:member": [
        {
          "@id": "string",
          "@type": "string",
          "createAt": "string",
          "email": "ava@example.com",
          "firstName": "Ava",
          "hasPassword": true,
          "id": 1,
          "lastName": "Chen",
          "optinAt": "string",
          "phone": "string",
          "status": {},
          "username": {}
        }
      ],
      "hydra:search": {
        "@type": "string",
        "hydra:mapping": [
          {
            "@type": "string",
            "property": "string",
            "required": true,
            "variable": "string"
          }
        ],
        "hydra:template": "string",
        "hydra:variableRepresentation": "string"
      },
      "hydra:totalItems": 1,
      "hydra:view": {
        "@id": "string",
        "@type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@context` | string |  |
| `@id` | string |  |
| `@type` | string |  |
| `hydra:member[].@id` | string |  |
| `hydra:member[].@type` | string |  |
| `hydra:member[].createAt` | string |  |
| `hydra:member[].email` | string |  |
| `hydra:member[].firstName` | string |  |
| `hydra:member[].hasPassword` | boolean |  |
| `hydra:member[].id` | number |  |
| `hydra:member[].lastName` | string |  |
| `hydra:member[].optinAt` | string |  |
| `hydra:member[].phone` | string |  |
| `hydra:member[].status` | object |  |
| `hydra:member[].username` | object |  |
| `hydra:search.@type` | string |  |
| `hydra:search.hydra:mapping[].@type` | string |  |
| `hydra:search.hydra:mapping[].property` | string |  |
| `hydra:search.hydra:mapping[].required` | boolean |  |
| `hydra:search.hydra:mapping[].variable` | string |  |
| `hydra:search.hydra:template` | string |  |
| `hydra:search.hydra:variableRepresentation` | string |  |
| `hydra:totalItems` | number |  |
| `hydra:view.@id` | string |  |
| `hydra:view.@type` | string |  |

## Native endpoint

Through the native Evalandgo API, this operation is `GET /api/v3/contacts` (base URL `https://app.evalandgo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

