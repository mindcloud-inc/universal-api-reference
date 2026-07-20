# CoachAccountable: List Offering Submissions

Retrieves offering submissions from CoachAccountable.

```
GET https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-offering-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-offering-submissions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-offering-submissions?${params}`, {
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
| `clientId` | number | no | Filter Offering Submissions by Client. |
| `offeringId` | number | no | Filter Offering Submissions by Offering. |
| `name` | string | no | Filter Offering Submissions by Offering by name, supports partial matching on prefix. |
| `dateFrom` | date | no | Set to restrict Offering Submissions returned to those at or after the provided value. |
| `dateTo` | date | no | Set to restrict Offering Submissions returned to those at or before the provided value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amountPaid": 1,
      "clientEmail": "ava@example.com",
      "ClientID": 1,
      "ClientInvoiceID": 1,
      "clientName": "Ava Chen",
      "dateAdded": "2026-05-07T12:00:00.000Z",
      "ID": 1,
      "OfferingID": 1,
      "offeringName": "Ava Chen",
      "trackingData": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountPaid` | number |  |
| `clientEmail` | string |  |
| `ClientID` | number |  |
| `ClientInvoiceID` | number |  |
| `clientName` | string |  |
| `dateAdded` | date |  |
| `ID` | number |  |
| `OfferingID` | number |  |
| `offeringName` | string |  |
| `trackingData` | string |  |

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-offering-submissions.md) for the provider-specific parameters and requirements.

