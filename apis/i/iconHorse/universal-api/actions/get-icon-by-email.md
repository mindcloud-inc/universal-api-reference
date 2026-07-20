# Icon Horse: Get Icon by Email

Retrieves a website icon from Icon Horse by email.

```
GET https://connect.mindcloud.co/v1/universal/iconHorse/latest/actions/get-icon-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Icon Horse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iconHorse/latest/actions/get-icon-by-email?connectionId=$CONNECTION_ID&email=hello%2540wikipedia.org" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "hello%40wikipedia.org"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iconHorse/latest/actions/get-icon-by-email?${params}`, {
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
| `email` | string | yes | URL-encoded email address to resolve into an icon, such as hello%40wikipedia.org. Default: `hello%40wikipedia.org`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Icon Horse API returns.

## Native endpoint

Through the native Icon Horse API, this operation is `GET /icon/:email` (base URL `https://icon.horse`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-icon-by-email.md) for the provider-specific parameters and requirements.

