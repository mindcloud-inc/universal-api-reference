# GoDaddy CRM: Create Shopper Subaccount

Creates a shopper subaccount in GoDaddy.

```
POST https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/create-shopper-subaccount
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoDaddy CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/create-shopper-subaccount" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "nameFirst": "Taylor",
  "nameLast": "Reed",
  "email": "shopper@example.com",
  "password": "TempPassw0rd!"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/create-shopper-subaccount', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "nameFirst": "Taylor",
    "nameLast": "Reed",
    "email": "shopper@example.com",
    "password": "TempPassw0rd!"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `nameFirst` | string | yes | Required shopper first name Example: `Taylor`. |
| `nameLast` | string | yes | Required shopper last name Example: `Reed`. |
| `email` | string | yes | Required subaccount email address Example: `shopper@example.com`. |
| `password` | string | yes | Required password for the new subaccount Example: `TempPassw0rd!`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `marketId` | string | no | Optional BCP-47 market identifier. Defaults to en-US. Default: `en-US`. Example: `en-US`. |
| `externalId` | number | no | Optional external numeric identifier for the subaccount Example: `12345`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GoDaddy CRM API returns.

## Native endpoint

Through the native GoDaddy CRM API, this operation is `POST /v1/shoppers/subaccount` (base URL `https://api.godaddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-shopper-subaccount.md) for the provider-specific parameters and requirements.

