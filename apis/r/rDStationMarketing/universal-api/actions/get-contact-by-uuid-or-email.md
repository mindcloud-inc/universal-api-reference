# RD Station Marketing: Get Contact by UUID or Email



```
GET https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/get-contact-by-uuid-or-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RD Station Marketing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/get-contact-by-uuid-or-email?connectionId=$CONNECTION_ID&identifier=email&value=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "email",
  "value": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/get-contact-by-uuid-or-email?${params}`, {
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
| `identifier` | list<string> | yes | Identifier type in path (uuid or email). One of: `email`, `uuid`. |
| `value` | string | yes | Identifier value in path. |

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

Through the native RD Station Marketing API, this operation is `GET /platform/contacts/:identifier::value` (base URL `https://api.rd.services`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-by-uuid-or-email.md) for the provider-specific parameters and requirements.

