# UniOne: Check Unsubscribed

Checks whether an email address is unsubscribed in UniOne.

```
GET https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/check-unsubscribed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UniOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/check-unsubscribed?connectionId=$CONNECTION_ID&address=user%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "user@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/check-unsubscribed?${params}`, {
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
| `address` | string | yes | Email address to check in the unsubscribed list. Example: `user@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "is_unsubscribed": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `is_unsubscribed` | boolean |  |
| `status` | string |  |

## Native endpoint

Through the native UniOne API, this operation is `POST unsubscribed/check.json` (base URL `https://api.unione.io/en/transactional/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-unsubscribed.md) for the provider-specific parameters and requirements.

