# Halo Service Solutions: Get Asset

Retrieves an asset from Halo Service Solutions.

```
GET https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Halo Service Solutions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-asset?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-asset?${params}`, {
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
| `id` | number | yes | Asset ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assettype_id": 1,
      "assettype_name": "Ava Chen",
      "client_id": 1,
      "client_name": "Ava Chen",
      "icon": "string",
      "id": 1,
      "inactive": true,
      "inventory_number": "string",
      "site_id": 1,
      "site_name": "Ava Chen",
      "status_id": 1,
      "supplier_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assettype_id` | number |  |
| `assettype_name` | string |  |
| `client_id` | number |  |
| `client_name` | string |  |
| `icon` | string |  |
| `id` | number | Asset ID |
| `inactive` | boolean |  |
| `inventory_number` | string |  |
| `site_id` | number |  |
| `site_name` | string |  |
| `status_id` | number |  |
| `supplier_id` | number |  |

## Native endpoint

Through the native Halo Service Solutions API, this operation is `GET /Asset/:id` (base URL `https://mindcloud.halopsa.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asset.md) for the provider-specific parameters and requirements.

