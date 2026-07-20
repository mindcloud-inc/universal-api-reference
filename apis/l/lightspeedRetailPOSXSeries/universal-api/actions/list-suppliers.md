# Lightspeed Retail POS (X-Series): List Suppliers

Retrieves suppliers from Lightspeed Retail POS (X-Series).

```
GET https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/list-suppliers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightspeed Retail POS (X-Series) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/list-suppliers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/list-suppliers?${params}`, {
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
      "contact": "string",
      "defaultMarkup": "string",
      "deletedAt": "string",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "source": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact` | string |  |
| `defaultMarkup` | string |  |
| `deletedAt` | string |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `source` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Lightspeed Retail POS (X-Series) API, this operation is `GET /api/2.0/suppliers` (base URL `https://{{credentials.authorizeRequest.domain_prefix}}.retail.lightspeed.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-suppliers.md) for the provider-specific parameters and requirements.

