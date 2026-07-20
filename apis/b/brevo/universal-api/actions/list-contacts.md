# Brevo: List Contacts



```
GET https://connect.mindcloud.co/v1/universal/brevo/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brevo/latest/actions/list-contacts?${params}`, {
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
| `limit` | number | no | Maximum records to return. |
| `offset` | number | no | Number of records to skip. |
| `sort` | string | no | Sort direction (asc or desc). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts": [
        {
          "createdAt": "string",
          "email": "ava@example.com",
          "emailBlacklisted": true,
          "id": 1,
          "listUnsubscribed": {},
          "modifiedAt": "string",
          "smsBlacklisted": true
        }
      ],
      "count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts[].createdAt` | string |  |
| `contacts[].email` | string |  |
| `contacts[].emailBlacklisted` | boolean |  |
| `contacts[].id` | number |  |
| `contacts[].listUnsubscribed` | object |  |
| `contacts[].modifiedAt` | string |  |
| `contacts[].smsBlacklisted` | boolean |  |
| `count` | number |  |

## Native endpoint

Through the native Brevo API, this operation is `GET /v3/contacts` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

