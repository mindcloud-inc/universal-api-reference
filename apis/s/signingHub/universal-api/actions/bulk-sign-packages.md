# SigningHub: Bulk Sign Packages

Signs packages in bulk in SigningHub.

```
POST https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/bulk-sign-packages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigningHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/bulk-sign-packages" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ids[]": "11191542",
  "handSignatureImage": "Base64 PNG or JPG signature image"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/bulk-sign-packages', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ids[]": "11191542",
    "handSignatureImage": "Base64 PNG or JPG signature image"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ids[]` | array<number> | yes | The document package IDs to bulk sign. Example: `11191542`. |
| `handSignatureImage` | string | yes | Base64-encoded hand signature image to apply when bulk signing. Example: `Base64 PNG or JPG signature image`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "transaction_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |
| `transaction_id` | string |  |

## Native endpoint

Through the native SigningHub API, this operation is `POST /v4/packages/SIGN` (base URL `https://api.signinghub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-sign-packages.md) for the provider-specific parameters and requirements.

