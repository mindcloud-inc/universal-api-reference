# profileAPI: Reverse Lookup Email

Finds a person in profileAPI by email address.

```
GET https://connect.mindcloud.co/v1/universal/profileAPI/latest/actions/reverse-lookup-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a profileAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/profileAPI/latest/actions/reverse-lookup-email?connectionId=$CONNECTION_ID&email=person%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "person@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/profileAPI/latest/actions/reverse-lookup-email?${params}`, {
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
| `email` | string | yes | Email address to reverse lookup. Example: `person@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "linkedInUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `linkedInUrl` | string |  |

## Native endpoint

Through the native profileAPI API, this operation is `POST /email-contacts/reverse-lookup` (base URL `https://api.profileapi.com/2024-03-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reverse-lookup-email.md) for the provider-specific parameters and requirements.

