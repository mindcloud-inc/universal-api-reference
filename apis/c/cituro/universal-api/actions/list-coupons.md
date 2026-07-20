# Cituro: List Coupons

Retrieves a list of coupons from Cituro.

```
GET https://connect.mindcloud.co/v1/universal/cituro/latest/actions/list-coupons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cituro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cituro/latest/actions/list-coupons?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cituro/latest/actions/list-coupons?${params}`, {
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
| `limit` | string | no | Maximum number of coupons to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Unique Cituro coupon identifier. |

## Native endpoint

Through the native Cituro API, this operation is `GET /coupons` (base URL `https://app.cituro.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-coupons.md) for the provider-specific parameters and requirements.

