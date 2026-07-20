# Cryptlex: Create Product

Creates a product in Cryptlex.

```
POST https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryptlex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "displayName": "Ava Chen",
  "description": "string",
  "licenseTemplateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "displayName": "Ava Chen",
    "description": "string",
    "licenseTemplateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Unique name for the product. |
| `displayName` | string | yes | Display name for the product. |
| `description` | string | yes | Description for the product. |
| `licenseTemplateId` | string | yes | License template to attach to the product. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "displayName": "Ava Chen",
      "id": "string",
      "licenseTemplateId": "string",
      "name": "Ava Chen",
      "totalLicenses": 1,
      "totalReleases": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `description` | string |  |
| `displayName` | string |  |
| `id` | string |  |
| `licenseTemplateId` | string |  |
| `name` | string |  |
| `totalLicenses` | number |  |
| `totalReleases` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Cryptlex API, this operation is `POST /v3/products` (base URL `https://api.cryptlex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

