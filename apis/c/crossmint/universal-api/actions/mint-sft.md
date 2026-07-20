# Crossmint: Mint SFT

Mints an SFT in Crossmint.

```
POST https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/mint-sft
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crossmint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/mint-sft" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "2b93e85e-d500-4f14-8a76-515c604e59ff",
  "templateId": "silver-pass",
  "recipient": "email:apps@mindcloud.co:polygon"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/mint-sft', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "2b93e85e-d500-4f14-8a76-515c604e59ff",
    "templateId": "silver-pass",
    "recipient": "email:apps@mindcloud.co:polygon"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionId` | string | yes | Collection identifier. Default: `2b93e85e-d500-4f14-8a76-515c604e59ff`. Example: `2b93e85e-d500-4f14-8a76-515c604e59ff`. |
| `templateId` | string | yes | SFT template identifier. Example: `silver-pass`. |
| `recipient` | string | yes | Recipient address. Example: `email:apps@mindcloud.co:polygon`. |
| `sendNotification` | boolean | no | Email notification flag. Default: `true`. |
| `amount` | number | no | Amount to mint. Default: `10`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `locale` | string | no | Locale for notification content. Default: `en-US`. Example: `en-US`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Crossmint API returns.

## Native endpoint

Through the native Crossmint API, this operation is `POST /2022-06-09/collections/:collectionId/sfts` (base URL `https://staging.crossmint.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mint-sft.md) for the provider-specific parameters and requirements.

