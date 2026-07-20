# Snappy: Get Variant

Retrieves a variant from Snappy.

```
GET https://connect.mindcloud.co/v1/universal/snappy/latest/actions/get-variant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snappy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snappy/latest/actions/get-variant?connectionId=$CONNECTION_ID&variantId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variantId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snappy/latest/actions/get-variant?${params}`, {
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
| `variantId` | string | yes | Variant ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | string | no | Company ID. |
| `country` | string | no | Country. Default: `US`. |
| `fields[]` | array<string> | no | Additional variant fields to include. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Snappy API returns.

## Native endpoint

Through the native Snappy API, this operation is `GET /variants/{variantId}` (base URL `https://api.snappy.com/public-api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-variant.md) for the provider-specific parameters and requirements.

