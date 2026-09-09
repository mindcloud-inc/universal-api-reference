# Walmart: Get Supported Carrier Package Types

Retrieves supported package types for a selected carrier.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-supported-carrier-package-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-supported-carrier-package-types?connectionId=$CONNECTION_ID&carrierShortName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "carrierShortName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-supported-carrier-package-types?${params}`, {
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
| `carrierShortName` | string | yes | Provide a `carrierShortName` or pass `ALL` to fetch all package types of supported carriers |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dimensionUnit": "string",
      "height": 1,
      "id": "string",
      "length": 1,
      "packageTypeDisplayName": "Ava Chen",
      "packageTypeShortName": "Ava Chen",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dimensionUnit` | string |  |
| `height` | number |  |
| `id` | string |  |
| `length` | number |  |
| `packageTypeDisplayName` | string |  |
| `packageTypeShortName` | string |  |
| `width` | number |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/shipping/labels/carriers/:carrierShortName/package-types` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-supported-carrier-package-types.md) for the provider-specific parameters and requirements.

