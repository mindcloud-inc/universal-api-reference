# Cryptlex: Update Product

Updates an existing product in Cryptlex.

```
PUT https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryptlex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/update-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Unique identifier for the product. |
| `name` | string | no | Unique name for the product. |
| `displayName` | string | no | Display name for the product. |
| `description` | string | no | Description for the product. |
| `automatedEmails` | list<string> | no | Automated emails enabled for the product. |
| `licenseTemplateId` | string | no | License template linked to the product. |
| `licensePolicyId` | string | no | License policy linked to the product. |
| `trialPolicyId` | string | no | Trial policy linked to the product. |

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

Through the native Cryptlex API, this operation is `PATCH /v3/products/:id` (base URL `https://api.cryptlex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product.md) for the provider-specific parameters and requirements.

