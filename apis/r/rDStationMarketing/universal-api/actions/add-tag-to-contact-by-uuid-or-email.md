# RD Station Marketing: Add Tag to Contact by UUID or Email



```
POST https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/add-tag-to-contact-by-uuid-or-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RD Station Marketing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/add-tag-to-contact-by-uuid-or-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identifier": "email",
  "tags[]": [
    "string"
  ],
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/add-tag-to-contact-by-uuid-or-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identifier": "email",
    "tags[]": ["string"],
    "value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identifier` | list<string> | yes | Identifier type in path (uuid or email). One of: `email`, `uuid`. |
| `tags[]` | array<string> | yes | Tags a serem adicionadas ao contato. |
| `value` | string | yes | Identifier value in path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bio": "string",
      "city": "string",
      "country": "string",
      "email": "ava@example.com",
      "extraEmails": [
        [
          "ava@example.com"
        ]
      ],
      "jobTitle": "string",
      "legalBases": [
        {
          "category": "string",
          "status": "string",
          "type": "string"
        }
      ],
      "linkedin": "https://example.com",
      "links": [
        {
          "href": "https://example.com"
        }
      ],
      "name": "Ava Chen",
      "personalPhone": "string",
      "state": "string",
      "tags": [
        [
          "string"
        ]
      ],
      "uuid": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bio` | string |  |
| `city` | string |  |
| `country` | string |  |
| `email` | string |  |
| `extraEmails[]` | array<string> |  |
| `jobTitle` | string |  |
| `legalBases[].category` | string |  |
| `legalBases[].status` | string |  |
| `legalBases[].type` | string |  |
| `linkedin` | string |  |
| `links[].href` | string |  |
| `name` | string |  |
| `personalPhone` | string |  |
| `state` | string |  |
| `tags[]` | array<string> |  |
| `uuid` | string |  |
| `website` | string |  |

## Native endpoint

Through the native RD Station Marketing API, this operation is `POST /platform/contacts/:identifier::value/tag` (base URL `https://api.rd.services`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-tag-to-contact-by-uuid-or-email.md) for the provider-specific parameters and requirements.

