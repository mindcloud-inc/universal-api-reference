# smsmode: Create Transfer



```
POST https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/create-transfer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smsmode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/create-transfer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organisationId": "string",
  "organisationDestination": {},
  "amount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/create-transfer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organisationId": "string",
    "organisationDestination": {},
    "amount": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organisationId` | string | yes | Organisation ID path parameter from the smsmode API route. |
| `organisationDestination` | object | yes | Destination Organisation request body field documented by the smsmode API. |
| `amount` | number | yes | Amount request body field documented by the smsmode API. |
| `reference` | string | no | Reference request body field documented by the smsmode API. |
| `description` | string | no | Description request body field documented by the smsmode API. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "description": "string",
      "href": "string",
      "organisationDestination": {
        "organisationId": "string"
      },
      "reference": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `description` | string |  |
| `href` | string |  |
| `organisationDestination.organisationId` | string |  |
| `reference` | string |  |

## Native endpoint

Through the native smsmode API, this operation is `POST commons/v1/organisations/:organisationId/transfers` (base URL `https://rest.smsmode.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transfer.md) for the provider-specific parameters and requirements.

