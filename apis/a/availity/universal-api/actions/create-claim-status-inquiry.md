# Availity: Create Claim Status Inquiry

Creates a claim status inquiry in Availity.

```
POST https://connect.mindcloud.co/v1/universal/availity/latest/actions/create-claim-status-inquiry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Availity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/availity/latest/actions/create-claim-status-inquiry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/availity/latest/actions/create-claim-status-inquiry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `claimStatus` | object | no | Claim status inquiry request body. For demo POST scenarios, Availity documents that an empty JSON body may be used. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "claimAmount": "string",
      "claimCount": "string",
      "controlNumber": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "customerId": "string",
      "expirationDate": "2026-05-07T12:00:00.000Z",
      "fromDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "links": {},
      "patient": {},
      "payer": {},
      "providers": [
        {}
      ],
      "status": "string",
      "statusCode": "string",
      "submitter": {},
      "subscriber": {},
      "toDate": "2026-05-07T12:00:00.000Z",
      "updatedDate": "2026-05-07T12:00:00.000Z",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `claimAmount` | string | Claim amount submitted in the inquiry. |
| `claimCount` | string | Number of matching claim status records. |
| `controlNumber` | string | Control number returned for the inquiry. |
| `createdDate` | date | Claim status inquiry creation timestamp. |
| `customerId` | string | Availity customer identifier for the claim status inquiry. |
| `expirationDate` | date | Claim status inquiry expiration timestamp. |
| `fromDate` | date | Claim service period start date. |
| `id` | string | Claim status inquiry identifier. |
| `links` | object | Related Availity links. |
| `patient` | object | Patient details. |
| `payer` | object | Payer details. |
| `providers` | array<object> | Provider details. |
| `status` | string | Claim status inquiry processing status. |
| `statusCode` | string | Claim status code. |
| `submitter` | object | Submitter details. |
| `subscriber` | object | Subscriber details. |
| `toDate` | date | Claim service period end date. |
| `updatedDate` | date | Claim status inquiry last update timestamp. |
| `userId` | string | Availity user identifier associated with the inquiry. |

## Native endpoint

Through the native Availity API, this operation is `POST /availity/v1/claim-statuses` (base URL `https://api.availity.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-claim-status-inquiry.md) for the provider-specific parameters and requirements.

