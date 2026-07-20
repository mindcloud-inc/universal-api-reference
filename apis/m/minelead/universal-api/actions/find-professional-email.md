# Minelead: Find Professional Email

Finds a professional email in Minelead by name and domain.

```
GET https://connect.mindcloud.co/v1/universal/minelead/latest/actions/find-professional-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Minelead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/minelead/latest/actions/find-professional-email?connectionId=$CONNECTION_ID&domain=string&firstname=Ava&lastname=Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string",
  "firstname": "Ava",
  "lastname": "Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/minelead/latest/actions/find-professional-email?${params}`, {
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
| `domain` | string | yes | Company domain for the person lookup. |
| `firstname` | string | yes | Person's first name. |
| `lastname` | string | yes | Person's last name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domain": "string",
      "email": "ava@example.com",
      "firstname": "Ava",
      "lastname": "Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain` | string |  |
| `email` | string |  |
| `firstname` | string |  |
| `lastname` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Minelead API, this operation is `GET /find` (base URL `https://api.minelead.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-professional-email.md) for the provider-specific parameters and requirements.

