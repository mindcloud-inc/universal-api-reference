# profileAPI: Reverse Lookup Phone

Finds a person in profileAPI by phone number.

```
GET https://connect.mindcloud.co/v1/universal/profileAPI/latest/actions/reverse-lookup-phone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a profileAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/profileAPI/latest/actions/reverse-lookup-phone?connectionId=$CONNECTION_ID&phone=%2B1234567890" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phone": "+1234567890"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/profileAPI/latest/actions/reverse-lookup-phone?${params}`, {
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
| `phone` | string | yes | E.164 phone number to reverse lookup. Example: `+1234567890`. |

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

Through the native profileAPI API, this operation is `POST /phone-contacts/reverse-lookup` (base URL `https://api.profileapi.com/2024-03-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reverse-lookup-phone.md) for the provider-specific parameters and requirements.

