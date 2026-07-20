# Strale: Get Solution

Retrieves a solution from Strale.

```
GET https://connect.mindcloud.co/v1/universal/strale/latest/actions/get-solution
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strale/latest/actions/get-solution?connectionId=$CONNECTION_ID&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strale/latest/actions/get-solution?${params}`, {
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
| `slug` | string | yes | Solution slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentDescription": "string",
      "category": "string",
      "componentSumCents": 1,
      "description": "string",
      "geography": "string",
      "longDescription": "string",
      "marketingName": "Ava Chen",
      "name": "Ava Chen",
      "priceCents": 1,
      "slug": "string",
      "targetAudience": "string",
      "transparencyTag": "string",
      "valueTier": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentDescription` | string | Search-oriented agent description. |
| `category` | string | Solution category. |
| `componentSumCents` | number | Combined price of component capabilities. |
| `description` | string | Short solution description. |
| `geography` | string | Geography scope. |
| `longDescription` | string | Detailed solution description. |
| `marketingName` | string | Optional marketing-facing name. |
| `name` | string | Solution name. |
| `priceCents` | number | Solution price in cents. |
| `slug` | string | Solution slug. |
| `targetAudience` | string | Primary target audience. |
| `transparencyTag` | string | Transparency classification. |
| `valueTier` | string | Provider value tier label. |

## Native endpoint

Through the native Strale API, this operation is `GET /v1/solutions/:slug` (base URL `https://api.strale.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-solution.md) for the provider-specific parameters and requirements.

