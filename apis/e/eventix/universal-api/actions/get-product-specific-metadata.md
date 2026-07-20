# Eventix: Get attached Metadata of Product Type

Retrieves metadata for an Eventix product type.

```
GET https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-product-specific-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-product-specific-metadata?connectionId=$CONNECTION_ID&guid=product-guid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guid": "product-guid"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-product-specific-metadata?${params}`, {
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
| `guid` | string | yes | The guid of the Product Type. Example: `product-guid`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "auto_fill_facebook": "string",
      "copy_on_swap": true,
      "extra": "string",
      "guid": "string",
      "name": "Ava Chen",
      "shop_description": "string",
      "translatable": true,
      "translate_name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auto_fill_facebook` | string |  |
| `copy_on_swap` | boolean |  |
| `extra` | string |  |
| `guid` | string |  |
| `name` | string |  |
| `shop_description` | string |  |
| `translatable` | boolean |  |
| `translate_name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Eventix API, this operation is `GET /3.0.0/product/:guid/metaData` (base URL `https://api.weeztix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-specific-metadata.md) for the provider-specific parameters and requirements.

