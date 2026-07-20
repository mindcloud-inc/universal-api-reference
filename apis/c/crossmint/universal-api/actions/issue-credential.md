# Crossmint: Issue Credential

Issues a credential in Crossmint.

```
POST https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/issue-credential
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crossmint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/issue-credential" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "2b93e85e-d500-4f14-8a76-515c604e59ff",
  "recipient": "email:apps@mindcloud.co:polygon",
  "credential": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/issue-credential', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "2b93e85e-d500-4f14-8a76-515c604e59ff",
    "recipient": "email:apps@mindcloud.co:polygon",
    "credential": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | Credential template identifier related to the new credential. Example: `2b93e85e-d500-4f14-8a76-515c604e59ff`. |
| `recipient` | string | yes | Recipient address in `<chain>:<address>` or `email:<email_address>:<chain>` format. Example: `email:apps@mindcloud.co:polygon`. |
| `credential` | object | yes | Credential payload object. Include `subject` and optional `expiresAt`. Example: `[object Object]`. |
| `sendNotification` | boolean | no | Notify the recipient by email after issuance. Defaults to true. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `locale` | string | no | Locale for notification content. Defaults to `en-US`. Default: `en-US`. Example: `en-US`. |
| `metadata` | object | no | Optional credential NFT metadata override object. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionId": "string",
      "credentialId": "string",
      "id": "string",
      "onChain": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionId` | string | Action identifier returned by Crossmint. |
| `credentialId` | string | Issued credential identifier. |
| `id` | string | Credential issuance transaction identifier. |
| `onChain` | object | On-chain issuance status. |

## Native endpoint

Through the native Crossmint API, this operation is `POST /v1-alpha1/credentials/templates/:templateId/vcs` (base URL `https://staging.crossmint.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/issue-credential.md) for the provider-specific parameters and requirements.

