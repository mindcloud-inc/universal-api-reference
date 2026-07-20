# Availity: Get Claim Status Inquiry

Retrieves a claim status inquiry from Availity.

```
GET https://connect.mindcloud.co/v1/universal/availity/latest/actions/get-claim-status-inquiry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Availity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/availity/latest/actions/get-claim-status-inquiry?connectionId=$CONNECTION_ID&id=123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/availity/latest/actions/get-claim-status-inquiry?${params}`, {
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
| `id` | string | yes | Unique response ID from the initial claim status inquiry request. Example: `123`. |

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

Through the native Availity API, this operation is `GET /availity/v1/claim-statuses/{id}` (base URL `https://api.availity.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-claim-status-inquiry.md) for the provider-specific parameters and requirements.

