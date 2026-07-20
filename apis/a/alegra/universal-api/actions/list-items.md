# Alegra: List Items

Retrieves items from your Alegra account.

```
GET https://connect.mindcloud.co/v1/universal/alegra/latest/actions/list-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alegra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alegra/latest/actions/list-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alegra/latest/actions/list-items?${params}`, {
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
| `start` | number | no |  |
| `limit` | number | no |  |
| `orderDirection` | string | no |  |
| `orderField` | string | no |  |
| `query` | string | no |  |
| `metadata` | boolean | no |  |
| `idWarehouse` | string | no |  |
| `name` | string | no |  |
| `reference` | string | no |  |
| `price` | string | no |  |
| `description` | string | no |  |
| `pricelistId` | string | no |  |
| `idItemCategory` | string | no |  |
| `type` | string | no |  |
| `variantattributeId` | string | no |  |
| `variantattributeoptionId` | string | no |  |
| `variantparentId` | string | no |  |
| `customfieldId` | string | no |  |
| `customfieldValue` | string | no |  |
| `status` | string | no |  |
| `inventariable` | boolean | no |  |
| `fields` | string | no |  |
| `mode` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Alegra API returns.

## Native endpoint

Through the native Alegra API, this operation is `GET /items` (base URL `https://api.alegra.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-items.md) for the provider-specific parameters and requirements.

