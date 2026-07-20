# PeopleDB: Validate Email Address via POST

Validates an email address in PeopleDB via POST.

```
POST https://connect.mindcloud.co/v1/universal/peopleDB/latest/actions/validate-email-address-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PeopleDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/peopleDB/latest/actions/validate-email-address-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emailAddress": "e.g. user@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/peopleDB/latest/actions/validate-email-address-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emailAddress": "e.g. user@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emailAddress` | string | yes | Email address to validate. Example: `e.g. user@example.com`. |
| `smtpTimeout` | number | no | SMTP check timeout in seconds. Example: `Default 10 seconds`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checks": {},
      "classification": "string",
      "email": "ava@example.com",
      "errors": [
        "string"
      ],
      "score": 1,
      "scoreDetails": {},
      "valid": true,
      "warnings": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checks` | object |  |
| `classification` | string |  |
| `email` | string |  |
| `errors` | array<string> |  |
| `score` | number |  |
| `scoreDetails` | object |  |
| `valid` | boolean |  |
| `warnings` | array<string> |  |

## Native endpoint

Through the native PeopleDB API, this operation is `POST /email_verifications` (base URL `https://peopledb.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-email-address-post.md) for the provider-specific parameters and requirements.

