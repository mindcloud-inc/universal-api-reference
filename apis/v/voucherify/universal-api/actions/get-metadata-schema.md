# Voucherify: Get Metadata Schema

Retrieves a metadata schema from Voucherify.

```
GET https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/get-metadata-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voucherify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/get-metadata-schema?connectionId=$CONNECTION_ID&relatedObject=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "relatedObject": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/get-metadata-schema?${params}`, {
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
| `relatedObject` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowDefinedOnly": true,
      "createdAt": "string",
      "id": "string",
      "object": "string",
      "properties": {},
      "relatedObject": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowDefinedOnly` | boolean |  |
| `createdAt` | string |  |
| `id` | string |  |
| `object` | string |  |
| `properties` | object |  |
| `relatedObject` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Voucherify API, this operation is `GET /metadata-schemas/:relatedObject` (base URL `https://us1.api.voucherify.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-metadata-schema.md) for the provider-specific parameters and requirements.

