# Giftbit: Retrieve Brand

Retrieves a reward brand from Giftbit.

```
GET https://connect.mindcloud.co/v1/universal/giftbit/latest/actions/retrieve-brand
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Giftbit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/giftbit/latest/actions/retrieve-brand?connectionId=$CONNECTION_ID&brandCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "brandCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/giftbit/latest/actions/retrieve-brand?${params}`, {
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
| `brandCode` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "brand": {},
      "info": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brand` | object |  |
| `info` | object |  |

## Native endpoint

Through the native Giftbit API, this operation is `GET /brands/:brand_code` (base URL `https://api-testbed.giftbit.com/papi/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-brand.md) for the provider-specific parameters and requirements.

