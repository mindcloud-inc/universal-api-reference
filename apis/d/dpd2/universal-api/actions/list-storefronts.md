# Dpd2: List Storefronts

Retrieves storefronts from your DPD account.

```
GET https://connect.mindcloud.co/v1/universal/dpd2/latest/actions/list-storefronts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dpd2 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dpd2/latest/actions/list-storefronts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dpd2/latest/actions/list-storefronts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "contact_email": "ava@example.com",
      "contact_name": "Ava Chen",
      "currency": "string",
      "id": 1,
      "name": "Ava Chen",
      "subdomain": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact_email` | string | Contact email. |
| `contact_name` | string | Contact name. |
| `currency` | string | Store currency. |
| `id` | number | Unique storefront ID. |
| `name` | string | Storefront name. |
| `subdomain` | string | DPD subdomain for v2 storefronts. |
| `type` | string | Storefront type. |
| `url` | string | Storefront URL when present. |

## Native endpoint

Through the native Dpd2 API, this operation is `GET /storefronts` (base URL `https://api.getdpd.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-storefronts.md) for the provider-specific parameters and requirements.

