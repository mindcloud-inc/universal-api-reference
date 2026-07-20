# Toofr: Get Prospect Profile

Retrieves a prospect profile from Toofr.

```
GET https://connect.mindcloud.co/v1/universal/toofr/latest/actions/get-prospect-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toofr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toofr/latest/actions/get-prospect-profile?connectionId=$CONNECTION_ID&email=ava%40example.com&firstName=Ava&lastName=Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com",
  "firstName": "Ava",
  "lastName": "Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toofr/latest/actions/get-prospect-profile?${params}`, {
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
| `email` | string | yes | Prospect email address. |
| `firstName` | string | yes | Prospect first name. |
| `lastName` | string | yes | Prospect last name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "last_name": "Chen",
      "linkedin_url": "https://example.com",
      "title": "string",
      "twitter_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `last_name` | string |  |
| `linkedin_url` | string |  |
| `title` | string |  |
| `twitter_url` | string |  |

## Native endpoint

Through the native Toofr API, this operation is `GET /profile` (base URL `https://www.findemails.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-prospect-profile.md) for the provider-specific parameters and requirements.

