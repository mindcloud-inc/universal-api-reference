# LeadDyno: Generate Affiliate Sign-In Link

Generates a time-limited sign-in link for an affiliate in LeadDyno.

```
GET https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/generate-affiliate-sign-in-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadDyno `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/generate-affiliate-sign-in-link?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/generate-affiliate-sign-in-link?${params}`, {
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
| `id` | number | yes | The affiliate ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliate_id": 1,
      "expires_at": "string",
      "expires_in_seconds": 1,
      "sign_in_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliate_id` | number |  |
| `expires_at` | string |  |
| `expires_in_seconds` | number |  |
| `sign_in_url` | string |  |

## Native endpoint

Through the native LeadDyno API, this operation is `POST /affiliates/:id/sign_in_link` (base URL `https://api.leaddyno.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-affiliate-sign-in-link.md) for the provider-specific parameters and requirements.

