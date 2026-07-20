# Control D: Create Custom Rule

Creates a custom rule in Control D.

```
POST https://connect.mindcloud.co/v1/universal/controlD/latest/actions/create-custom-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Control D `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/controlD/latest/actions/create-custom-rule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "profileId": "string",
  "do": 1,
  "status": 1,
  "hostnames[]": [
    "Ava Chen"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/controlD/latest/actions/create-custom-rule', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "profileId": "string",
    "do": 1,
    "status": 1,
    "hostnames[]": ["Ava Chen"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `profileId` | string | yes | Primary key (PK) of the profile |
| `do` | number | yes | Rule type. 0 = BLOCK. 1 = BYPASS, 2 = SPOOF, 3 = REDIRECT. <<glossary:Do>> |
| `status` | number | yes | Status of the rule |
| `via` | string | no | Spoof/Redirect target. If SPOOF, this can be an IPv4 or hostname. If REDIRECT, this must be a valid proxy identifier. <<glossary:Via>> |
| `viaV6` | string | no | If SPOOF this can be a valid IPv6 address (AAAA record) |
| `group` | number | no | Optional ID of the folder to create this rule in, root folder if ommited |
| `hostnames[]` | array<string> | yes | Array of hostnames |

## Response

```json
{
  "success": true,
  "data": [
    {
      "do": 1,
      "group": 1,
      "order": 1,
      "status": 1,
      "via": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `do` | number |  |
| `group` | number |  |
| `order` | number |  |
| `status` | number |  |
| `via` | string |  |

## Native endpoint

Through the native Control D API, this operation is `POST /profiles/:profileId/rules` (base URL `https://api.controld.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-rule.md) for the provider-specific parameters and requirements.

