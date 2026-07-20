# UserCheck: Get Blocklisted Domain

Retrieves a blocklisted domain from UserCheck.

```
GET https://connect.mindcloud.co/v1/universal/userCheck/latest/actions/get-blocklisted-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UserCheck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userCheck/latest/actions/get-blocklisted-domain?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userCheck/latest/actions/get-blocklisted-domain?${params}`, {
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
| `domain` | string | yes | Domain to check in the blocklist. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "domain": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `domain` | string |  |

## Native endpoint

Through the native UserCheck API, this operation is `GET /blocklist/:domain` (base URL `https://api.usercheck.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-blocklisted-domain.md) for the provider-specific parameters and requirements.

