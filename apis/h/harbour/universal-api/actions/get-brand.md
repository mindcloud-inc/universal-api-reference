# Harbour: Get Brand

Retrieves a specific brand from Harbour.

```
GET https://connect.mindcloud.co/v1/universal/harbour/latest/actions/get-brand
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harbour `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harbour/latest/actions/get-brand?connectionId=$CONNECTION_ID&brand_id=BRAND-AbCd" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "brand_id": "BRAND-AbCd"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harbour/latest/actions/get-brand?${params}`, {
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
| `brand_id` | string | yes | Unique Harbour brand identifier. Example: `BRAND-AbCd`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "brand": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brand` | object |  |

## Native endpoint

Through the native Harbour API, this operation is `GET https://api.harbourshare.com/v1/organizations/brands/:brand_id` (base URL `https://api.myharbourshare.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-brand.md) for the provider-specific parameters and requirements.

