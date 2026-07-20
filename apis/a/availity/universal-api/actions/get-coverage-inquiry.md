# Availity: Get Coverage Inquiry

Retrieves a coverage inquiry from Availity.

```
GET https://connect.mindcloud.co/v1/universal/availity/latest/actions/get-coverage-inquiry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Availity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/availity/latest/actions/get-coverage-inquiry?connectionId=$CONNECTION_ID&id=123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/availity/latest/actions/get-coverage-inquiry?${params}`, {
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
| `id` | string | yes | Unique response ID from the initial coverage inquiry request. Example: `123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asOfDate": "2026-05-07T12:00:00.000Z",
      "controlNumber": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "customerId": "string",
      "expirationDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "links": {},
      "patient": {},
      "payer": {},
      "plans": [
        {}
      ],
      "requestedServiceType": [
        {}
      ],
      "requestingProvider": {},
      "status": "string",
      "statusCode": "string",
      "subscriber": {},
      "updatedDate": "2026-05-07T12:00:00.000Z",
      "validationMessages": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asOfDate` | date | Eligibility as-of date. |
| `controlNumber` | string | Control number returned for the inquiry. |
| `createdDate` | date | Coverage inquiry creation timestamp. |
| `customerId` | string | Availity customer identifier for the coverage inquiry. |
| `expirationDate` | date | Coverage inquiry expiration timestamp. |
| `id` | string | Coverage inquiry identifier. |
| `links` | object | Related Availity links. |
| `patient` | object | Patient details. |
| `payer` | object | Payer details. |
| `plans` | array<object> | Coverage plan details. |
| `requestedServiceType` | array<object> | Requested service type details. |
| `requestingProvider` | object | Requesting provider details. |
| `status` | string | Coverage inquiry processing status. |
| `statusCode` | string | Coverage inquiry status code. |
| `subscriber` | object | Subscriber details. |
| `updatedDate` | date | Coverage inquiry last update timestamp. |
| `validationMessages` | array<object> | Validation messages returned by Availity. |

## Native endpoint

Through the native Availity API, this operation is `GET /v1/coverages/{id}` (base URL `https://api.availity.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-coverage-inquiry.md) for the provider-specific parameters and requirements.

