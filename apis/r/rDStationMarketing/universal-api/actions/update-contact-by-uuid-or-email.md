# RD Station Marketing: Update Contact by UUID or Email



```
PUT https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/update-contact-by-uuid-or-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RD Station Marketing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/update-contact-by-uuid-or-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identifier": "email",
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/update-contact-by-uuid-or-email', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identifier": "email",
    "value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bio` | string | no | Anotações sobre contato. |
| `birthdate` | string | no | Data de aniversário. |
| `city` | string | no | Cidade do contato. |
| `country` | string | no | País do contato. |
| `email` | string | no | Email do contato. |
| `facebook` | string | no | Facebook do contato. |
| `identifier` | list<string> | yes | Identifier type in path (uuid or email). One of: `email`, `uuid`. |
| `job_title` | string | no | Cargo do contato. |
| `legal_bases[]` | array<object> | no | Bases legais do contato. |
| `legal_bases[].category` | list<string> | no | Categoria da base legal (ex.: communications). One of: `communications`, `data_processing`. |
| `legal_bases[].status` | list<string> | no | Status da base legal (ex.: granted). One of: `declined`, `granted`. |
| `legal_bases[].type` | list<string> | no | Tipo da base legal (ex.: consent). One of: `consent`, `judicial_process`, `legitimate_interest`, `pre_existent_contract`, `public_interest`, `vital_interest`. |
| `linkedin` | string | no | LinkedIn do contato. |
| `mobile_phone` | string | no | Celular do contato. |
| `name` | string | no | Nome do contato. |
| `personal_phone` | string | no | Telefone do contato. |
| `state` | string | no | Estado do contato. |
| `tags[]` | array<string> | no | Tags do contato. |
| `twitter` | string | no | Twitter do contato. |
| `value` | string | yes | Identifier value in path. |
| `website` | string | no | Site do contato. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "birthdate": "2026-05-07T12:00:00.000Z",
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
      "links": [
        {
          "href": "https://example.com"
        }
      ],
      "mobilePhone": "string",
      "name": "Ava Chen",
      "personalPhone": "string",
      "state": "string",
      "tags": [
        [
          "string"
        ]
      ],
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `birthdate` | date |  |
| `city` | string |  |
| `country` | string |  |
| `email` | string |  |
| `extraEmails[]` | array<string> |  |
| `jobTitle` | string |  |
| `legalBases[].category` | string |  |
| `legalBases[].status` | string |  |
| `legalBases[].type` | string |  |
| `links[].href` | string |  |
| `mobilePhone` | string |  |
| `name` | string |  |
| `personalPhone` | string |  |
| `state` | string |  |
| `tags[]` | array<string> |  |
| `uuid` | string |  |

## Native endpoint

Through the native RD Station Marketing API, this operation is `PATCH /platform/contacts/:identifier::value` (base URL `https://api.rd.services`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-by-uuid-or-email.md) for the provider-specific parameters and requirements.

