# Routee: Update the IP whitelisting of API

Updates API IP whitelisting in Routee.

```
PUT https://connect.mindcloud.co/v1/universal/routee/latest/actions/update-the-ip-whitelisting-of-api
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/routee/latest/actions/update-the-ip-whitelisting-of-api" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "whitelistedIps[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/update-the-ip-whitelisting-of-api', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "whitelistedIps[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `whitelistedIps[]` | array<string> | yes | [Required, not empty] An Array of valid ip’s that will be used as whitelisted for using the API for the specific application. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "whitelistedIps": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `whitelistedIps[]` | array<string> |  |

## Native endpoint

Through the native Routee API, this operation is `PATCH /security/whitelist` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-the-ip-whitelisting-of-api.md) for the provider-specific parameters and requirements.

