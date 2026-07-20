# Crossmint: Create Credential Template

Creates a credential template in Crossmint.

```
POST https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/create-credential-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crossmint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/create-credential-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "metadata": "[object Object]",
  "chain": "polygon",
  "credentials": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/create-credential-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "metadata": "[object Object]",
    "chain": "polygon",
    "credentials": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metadata` | object | yes | Template metadata object. Provide `name`, `description`, and `imageUrl`. Example: `[object Object]`. |
| `chain` | string | yes | Chain for the credential NFT. Crossmint documents values such as `polygon`, `optimism`, and `base`. Default: `polygon`. Example: `polygon`. |
| `credentials` | object | yes | Credential template configuration object. Include `type`, `storage`, and `encryption`. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionId": "string",
      "fungibility": "string",
      "id": "string",
      "metadata": {},
      "onChain": {},
      "subscription": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionId` | string | Action identifier returned by Crossmint. |
| `fungibility` | string | Fungibility mode returned by Crossmint. |
| `id` | string | Credential template identifier returned by Crossmint. |
| `metadata` | object | Metadata for the created credential template. |
| `onChain` | object | On-chain configuration for the template. |
| `subscription` | object | Subscription settings for the template. |

## Native endpoint

Through the native Crossmint API, this operation is `POST /v1-alpha1/credentials/templates` (base URL `https://staging.crossmint.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-credential-template.md) for the provider-specific parameters and requirements.

