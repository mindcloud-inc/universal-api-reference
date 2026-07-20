# One-Time Secret: Private Update Receipt

Updates a private receipt in One-Time Secret.

```
PUT https://connect.mindcloud.co/v1/universal/oneTimeSecret/latest/actions/v2-private-update-receipt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a One-Time Secret `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oneTimeSecret/latest/actions/v2-private-update-receipt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneTimeSecret/latest/actions/v2-private-update-receipt', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identifier": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identifier` | string | yes | Private receipt identifier to update. |
| `memo` | string | no | Optional memo text to store on the private receipt. One-Time Secret supports up to 500 characters. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": {},
      "record": {},
      "shrimp": "string",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details` | object | Private receipt update details. |
| `record` | object | Updated private receipt record. |
| `shrimp` | string | Provider response marker when returned. |
| `user_id` | string | Authenticated user identifier when returned. |

## Native endpoint

Through the native One-Time Secret API, this operation is `PATCH /api/v2/private/:identifier` (base URL `https://us.onetimesecret.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/v2-private-update-receipt.md) for the provider-specific parameters and requirements.

