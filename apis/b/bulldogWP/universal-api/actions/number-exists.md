# Bulldog-WP: Check number exists

Checks whether phone numbers exist in Bulldog-WP.

```
GET https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/number-exists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bulldog-WP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/number-exists?connectionId=$CONNECTION_ID&phone=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phone": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/number-exists?${params}`, {
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
| `phone` | string | yes | Phone number to check for WhatsApp availability. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "businessInfo": {},
      "country": {},
      "exists": true,
      "isBusiness": true,
      "link": "https://example.com",
      "phone": "string",
      "wid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `businessInfo` | object |  |
| `country` | object |  |
| `exists` | boolean |  |
| `isBusiness` | boolean |  |
| `link` | string |  |
| `phone` | string |  |
| `wid` | string |  |

## Native endpoint

Through the native Bulldog-WP API, this operation is `POST /numbers/exists` (base URL `https://api.bulldog-wp.co.il/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/number-exists.md) for the provider-specific parameters and requirements.

