# Halo Service Solutions: Create Asset

Creates a new asset in Halo Service Solutions.

```
POST https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Halo Service Solutions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-asset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inventory_number": "string",
  "site_id": 1,
  "assettype_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-asset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inventory_number": "string",
    "site_id": 1,
    "assettype_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inventory_number` | string | yes |  |
| `site_id` | number | yes |  |
| `assettype_id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assettype_id": 1,
      "assettype_name": "Ava Chen",
      "client_id": 1,
      "id": 1,
      "inactive": true,
      "inventory_number": "string",
      "last_modified": "2026-05-07T12:00:00.000Z",
      "site_id": 1,
      "site_name": "Ava Chen",
      "status_id": 1
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
| `id` | number |  |
| `inactive` | boolean |  |
| `inventory_number` | string |  |
| `last_modified` | date |  |
| `site_id` | number |  |
| `site_name` | string |  |
| `status_id` | number |  |

## Native endpoint

Through the native Halo Service Solutions API, this operation is `POST /Asset` (base URL `https://mindcloud.halopsa.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-asset.md) for the provider-specific parameters and requirements.

