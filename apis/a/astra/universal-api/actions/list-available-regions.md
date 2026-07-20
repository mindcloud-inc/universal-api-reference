# Astra: List Available Regions

Retrieves available Astra serverless regions.

```
GET https://connect.mindcloud.co/v1/universal/astra/latest/actions/list-available-regions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Astra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/astra/latest/actions/list-available-regions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/astra/latest/actions/list-available-regions?${params}`, {
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
| `filterByOrg` | boolean | no | When true, return only regions enabled for the caller organization. |
| `regionType` | string | no | Optional region type filter such as all or vector. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "classification": "string",
      "cloudProvider": "string",
      "displayName": "Ava Chen",
      "enabled": true,
      "name": "Ava Chen",
      "pcu_types": [
        {}
      ],
      "region_type": "string",
      "reservedForQualifiedUsers": true,
      "zone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `classification` | string | The region classification. |
| `cloudProvider` | string | The cloud provider. |
| `displayName` | string | The user-facing region name. |
| `enabled` | boolean | Whether the region is enabled. |
| `name` | string | The region code. |
| `pcu_types` | array<object> | Available PCU shapes in the region. |
| `region_type` | string | The Astra region type. |
| `reservedForQualifiedUsers` | boolean | Whether the region is reserved for qualified users. |
| `zone` | string | The broad geography zone. |

## Native endpoint

Through the native Astra API, this operation is `GET /v2/regions/serverless` (base URL `https://api.astra.datastax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-available-regions.md) for the provider-specific parameters and requirements.

