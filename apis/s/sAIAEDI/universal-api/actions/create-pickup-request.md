# SAIA EDI: Create Pickup Request

Creates a pickup request in SAIA EDI.

```
POST https://connect.mindcloud.co/v1/universal/sAIAEDI/latest/actions/create-pickup-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SAIA EDI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sAIAEDI/latest/actions/create-pickup-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "AccountNumber": "string",
  "PickupDate": "string",
  "ReadyTime": "string",
  "CloseTime": "string",
  "TotalPieces": "string",
  "TotalWeight": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sAIAEDI/latest/actions/create-pickup-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "AccountNumber": "string",
    "PickupDate": "string",
    "ReadyTime": "string",
    "CloseTime": "string",
    "TotalPieces": "string",
    "TotalWeight": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `AccountNumber` | string | yes | Saia account number for pickup. |
| `PickupDate` | string | yes | Pickup date in YYYY-MM-DD format. |
| `ReadyTime` | string | yes | Ready time in HH:MM:SS format. |
| `CloseTime` | string | yes | Close time in HH:MM:SS format. |
| `TotalPieces` | string | yes | Total pieces for pickup. |
| `TotalWeight` | string | yes | Total shipment weight. |
| `CompanyName` | string | no | Pickup location company name. |
| `Street` | string | no | Pickup street address. |
| `City` | string | no | Pickup city. |
| `State` | string | no | Pickup state abbreviation. |
| `Zipcode` | string | no | Pickup ZIP code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Code": "string",
      "Element": "string",
      "Fault": "string",
      "Message": "string",
      "NextBusinessDate": "string",
      "PickupNumber": "string",
      "PickupTerminal": {},
      "TestMode": "string",
      "TotalPieces": 1,
      "TotalWeight": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Code` | string | Saia error code; blank indicates no documented error. |
| `Element` | string | Element associated with an error when available. |
| `Fault` | string | Fault classification returned by Saia. |
| `Message` | string | Error or status message. |
| `NextBusinessDate` | string | Next available business date when returned. |
| `PickupNumber` | string | Pickup confirmation number when returned by Saia. |
| `PickupTerminal` | object | Terminal details associated with the pickup request. |
| `TestMode` | string | Y or N test-mode flag echoed by Saia. |
| `TotalPieces` | number | Total pickup piece count. |
| `TotalWeight` | number | Total pickup weight. |

## Native endpoint

Through the native SAIA EDI API, this operation is `POST /webservice/pickup/xml.aspx` (base URL `https://www.saiasecure.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pickup-request.md) for the provider-specific parameters and requirements.

