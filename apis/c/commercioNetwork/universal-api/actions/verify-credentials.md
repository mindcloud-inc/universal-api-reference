# CommercioNetwork: Verify Credentials

Retrieves credential verification details from CommercioNetwork.

```
GET https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/verify-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CommercioNetwork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/verify-credentials?connectionId=$CONNECTION_ID&address=did%3Acom%3A..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "did:com:..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/verify-credentials?${params}`, {
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
| `address` | string | yes | The Commercio DID or wallet address to inspect for eKYC status. Example: `did:com:...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credentials": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credentials` | array<object> | The eKYC credential statuses available for the wallet address. |

## Native endpoint

Through the native CommercioNetwork API, this operation is `GET /eKYC/:address` (base URL `https://dev-api.commercio.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-credentials.md) for the provider-specific parameters and requirements.

