# Apple Map Links: Show Place By Address

Shows an Apple Maps place card by address.

```
GET https://connect.mindcloud.co/v1/universal/appleMapLinks/latest/actions/show-place-by-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apple Map Links `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appleMapLinks/latest/actions/show-place-by-address?connectionId=$CONNECTION_ID&address=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appleMapLinks/latest/actions/show-place-by-address?${params}`, {
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
| `address` | string | yes | Address string for the place card. |
| `map` | string | no | Optional map type: explore, driving, transit, satellite, or hybrid. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `url` | string | Generated Apple Maps URL. |

## Native endpoint

Through the native Apple Map Links API, this operation is `GET /place` (base URL `https://maps.apple.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/show-place-by-address.md) for the provider-specific parameters and requirements.

