# SigningHub: Validate Bulk Sign Packages

Validates packages for bulk signing in SigningHub.

```
POST https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/validate-bulk-sign-packages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigningHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/validate-bulk-sign-packages" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ids[]": "11191542"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/validate-bulk-sign-packages', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ids[]": "11191542"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ids[]` | array<number> | yes | The document package IDs to validate for bulk signing. Example: `11191542`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "failed_packages": [
        {}
      ],
      "success_packages": [
        {}
      ],
      "tasks": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `failed_packages` | array<object> |  |
| `success_packages` | array<object> |  |
| `tasks` | object |  |

## Native endpoint

Through the native SigningHub API, this operation is `POST /v4/packages/SIGN/pre` (base URL `https://api.signinghub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-bulk-sign-packages.md) for the provider-specific parameters and requirements.

