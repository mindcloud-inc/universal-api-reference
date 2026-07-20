# Kladana: Get Product Metadata

Retrieves product metadata details from Kladana.

```
GET https://connect.mindcloud.co/v1/universal/kladana/latest/actions/get-product-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kladana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kladana/latest/actions/get-product-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kladana/latest/actions/get-product-metadata?${params}`, {
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
      "attributes": [
        {}
      ],
      "createShared": true,
      "customEntityMeta": {},
      "meta": {},
      "states": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | array<object> | Custom product attributes. |
| `createShared` | boolean | Default shared-creation setting. |
| `customEntityMeta` | object | Custom entity metadata. |
| `meta` | object | Product metadata reference. |
| `states` | array<object> | Available states. |

## Native endpoint

Through the native Kladana API, this operation is `GET /entity/product/metadata` (base URL `https://api.kladana.com/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-metadata.md) for the provider-specific parameters and requirements.

