# Evalandgo: List Contact Respondents

Retrieves respondents for a contact from Evalandgo.

```
GET https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/list-contact-respondents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evalandgo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/list-contact-respondents?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/list-contact-respondents?${params}`, {
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
| `contactId` | string | yes | Contact identifier |
| `email` | string | no |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `finish` | boolean | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `withResponse` | string | no |  |
| `orderStartAt` | string | no |  |
| `orderEndAt` | string | no |  |
| `orderId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@context": "string",
      "@id": "string",
      "@type": "string",
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
      "hydra:totalItems": 1
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
| `hydra:search.@type` | string |  |
| `hydra:search.hydra:mapping[].@type` | string |  |
| `hydra:search.hydra:mapping[].property` | string |  |
| `hydra:search.hydra:mapping[].required` | boolean |  |
| `hydra:search.hydra:mapping[].variable` | string |  |
| `hydra:search.hydra:template` | string |  |
| `hydra:search.hydra:variableRepresentation` | string |  |
| `hydra:totalItems` | number |  |

## Native endpoint

Through the native Evalandgo API, this operation is `GET /api/v3/contacts/:contactId/respondents` (base URL `https://app.evalandgo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-respondents.md) for the provider-specific parameters and requirements.

