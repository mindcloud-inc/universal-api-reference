# Envoice: Create Estimation

Creates a new estimation in Envoice.

```
POST https://connect.mindcloud.co/v1/universal/envoice/latest/actions/create-estimation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/envoice/latest/actions/create-estimation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": 1,
  "currencyId": 1,
  "expiresOn": "2026-05-07T12:00:00.000Z",
  "issuedOn": "2026-05-07T12:00:00.000Z",
  "items": "string",
  "number": "string",
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/envoice/latest/actions/create-estimation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": 1,
    "currencyId": 1,
    "expiresOn": "2026-05-07T12:00:00.000Z",
    "issuedOn": "2026-05-07T12:00:00.000Z",
    "items": "string",
    "number": "string",
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | number | yes | Client identifier for the estimation. |
| `currencyId` | number | yes | Currency identifier. |
| `expiresOn` | date | yes | Estimation expiration date. |
| `issuedOn` | date | yes | Estimation issue date. |
| `items` | string | yes | JSON array of estimation item objects. |
| `notes` | string | no | Internal estimation notes. |
| `number` | string | yes | Unique estimation number. |
| `paymentGateways` | string | no | JSON array of estimation payment gateway objects. |
| `status` | string | yes | Estimation status. |
| `terms` | string | no | Estimation terms. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Client": {},
      "Id": 1,
      "Items": [
        {}
      ],
      "Number": "string",
      "Status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Client` | object | Estimation client. |
| `Id` | number | Estimation identifier. |
| `Items` | array<object> | Estimation line items. |
| `Number` | string | Estimation number. |
| `Status` | string | Estimation status. |

## Native endpoint

Through the native Envoice API, this operation is `POST estimation/new` (base URL `https://www.envoice.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-estimation.md) for the provider-specific parameters and requirements.

