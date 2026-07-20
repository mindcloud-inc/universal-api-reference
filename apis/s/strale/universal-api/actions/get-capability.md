# Strale: Get Capability

Retrieves a capability from Strale.

```
GET https://connect.mindcloud.co/v1/universal/strale/latest/actions/get-capability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strale/latest/actions/get-capability?connectionId=$CONNECTION_ID&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strale/latest/actions/get-capability?${params}`, {
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
| `slug` | string | yes | Capability slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "dataSource": "string",
      "description": "string",
      "geography": "string",
      "isFreeTier": true,
      "name": "Ava Chen",
      "priceCents": 1,
      "slug": "string",
      "transparencyTag": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string | Capability category. |
| `dataSource` | string | Primary data source description. |
| `description` | string | Capability description. |
| `geography` | string | Geography scope. |
| `isFreeTier` | boolean | Whether the capability is available in a free tier. |
| `name` | string | Capability name. |
| `priceCents` | number | Capability price in cents. |
| `slug` | string | Capability slug. |
| `transparencyTag` | string | Transparency classification. |

## Native endpoint

Through the native Strale API, this operation is `GET /v1/capabilities/:slug` (base URL `https://api.strale.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-capability.md) for the provider-specific parameters and requirements.

