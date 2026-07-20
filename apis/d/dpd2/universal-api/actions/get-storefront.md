# Dpd2: Get Storefront

Retrieves a storefront from DPD by ID.

```
GET https://connect.mindcloud.co/v1/universal/dpd2/latest/actions/get-storefront
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dpd2 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dpd2/latest/actions/get-storefront?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dpd2/latest/actions/get-storefront?${params}`, {
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
| `id` | number | yes | Unique storefront ID. |

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

Through the native Dpd2 API, this operation is `GET /storefronts/:id` (base URL `https://api.getdpd.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-storefront.md) for the provider-specific parameters and requirements.

