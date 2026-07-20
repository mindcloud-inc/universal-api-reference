# Oxylabs: Get Amazon Product

Retrieves Amazon product details with Oxylabs.

```
GET https://connect.mindcloud.co/v1/universal/oxylabs/latest/actions/get-amazon-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oxylabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oxylabs/latest/actions/get-amazon-product?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oxylabs/latest/actions/get-amazon-product?${params}`, {
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
| `query` | string | yes | Amazon ASIN to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "job": {},
      "results": [
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
| `job` | object | Oxylabs realtime job metadata for the request. |
| `results` | array<object> | Result rows returned by the selected Oxylabs source. |

## Native endpoint

Through the native Oxylabs API, this operation is `POST /v1/queries` (base URL `https://realtime.oxylabs.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-amazon-product.md) for the provider-specific parameters and requirements.

