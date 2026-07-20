# CommercioNetwork: Request SPID Session

Creates a SPID session in CommercioNetwork.

```
POST https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/request-spid-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CommercioNetwork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/request-spid-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "successUrl": "https://mindcloud.invalid/commercio/spid-success"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/request-spid-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "successUrl": "https://mindcloud.invalid/commercio/spid-success"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `successUrl` | string | yes | URL that Commercio should redirect to after a successful SPID authentication. Example: `https://mindcloud.invalid/commercio/spid-success`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authentication_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authentication_url` | string | The redirect URL where the user can complete the SPID authentication flow. |

## Native endpoint

Through the native CommercioNetwork API, this operation is `POST /eKYC/spid` (base URL `https://dev-api.commercio.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-spid-session.md) for the provider-specific parameters and requirements.

