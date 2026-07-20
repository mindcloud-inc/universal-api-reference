# Loomio: Check Email Exists

Checks whether an email exists in Loomio.

```
GET https://connect.mindcloud.co/v1/universal/loomio/latest/actions/check-email-exists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loomio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loomio/latest/actions/check-email-exists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loomio/latest/actions/check-email-exists?${params}`, {
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
| `email` | string | no | The email address to check. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "meta": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `meta` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native Loomio API, this operation is `GET /profile/email_exists` (base URL `https://www.loomio.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-email-exists.md) for the provider-specific parameters and requirements.

