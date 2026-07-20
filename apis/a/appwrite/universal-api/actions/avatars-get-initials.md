# Appwrite: Get user initials

Retrieves a user initials avatar from Appwrite.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/avatars-get-initials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/avatars-get-initials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/avatars-get-initials?${params}`, {
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
| `name` | string | no | Full Name. When empty, current user name or email will be used. Max length: 128 chars. |
| `width` | number | no | Image width. Pass an integer between 0 to 2000. Defaults to 100. |
| `height` | number | no | Image height. Pass an integer between 0 to 2000. Defaults to 100. |
| `background` | string | no | Changes background color. By default a random color will be picked and stay will persistent to the given name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object | Provider response payload. |

## Native endpoint

Through the native Appwrite API, this operation is `GET /avatars/initials` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/avatars-get-initials.md) for the provider-specific parameters and requirements.

