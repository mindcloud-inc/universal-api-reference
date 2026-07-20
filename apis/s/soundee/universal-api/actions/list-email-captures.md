# Soundee: List Email Captures

Retrieves captured email records from Soundee.

```
GET https://connect.mindcloud.co/v1/universal/soundee/latest/actions/list-email-captures
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Soundee `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/soundee/latest/actions/list-email-captures?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/soundee/latest/actions/list-email-captures?${params}`, {
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
| `listType` | string | no | Filter email captures by source type. |
| `search` | string | no | Search captures by email, first name, last name, or phone. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "email": "ava@example.com",
      "event": {},
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "ip": "string",
      "isCustomer": 1,
      "lastName": "Chen",
      "parameters": {},
      "phone": "string",
      "store": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number |  |
| `email` | string |  |
| `event` | object |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `ip` | string |  |
| `isCustomer` | number |  |
| `lastName` | string |  |
| `parameters` | object |  |
| `phone` | string |  |
| `store` | object |  |

## Native endpoint

Through the native Soundee API, this operation is `GET /email-captures` (base URL `https://api.soundee.com/me`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-email-captures.md) for the provider-specific parameters and requirements.

