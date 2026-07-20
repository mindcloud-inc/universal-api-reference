# Availity: Get Professional Predetermination

Retrieves a professional predetermination from Availity.

```
GET https://connect.mindcloud.co/v1/universal/availity/latest/actions/get-professional-predetermination
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Availity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/availity/latest/actions/get-professional-predetermination?connectionId=$CONNECTION_ID&id=123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/availity/latest/actions/get-professional-predetermination?${params}`, {
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
| `id` | string | yes | Unique response ID from the initial professional predetermination request. Example: `123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingProvider": {},
      "claimInformation": {},
      "createdDate": "2026-05-07T12:00:00.000Z",
      "expirationDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "patient": {},
      "payer": {},
      "requestTypeCode": "string",
      "submitter": {},
      "subscriber": {},
      "updatedDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingProvider` | object | Billing provider details. |
| `claimInformation` | object | Professional claim and service-line result details. |
| `createdDate` | date | Predetermination creation timestamp. |
| `expirationDate` | date | Predetermination expiration timestamp. |
| `id` | string | Professional predetermination identifier. |
| `patient` | object | Patient details. |
| `payer` | object | Payer details. |
| `requestTypeCode` | string | Request type code returned by Availity. |
| `submitter` | object | Submitter details. |
| `subscriber` | object | Subscriber and deductible details. |
| `updatedDate` | date | Predetermination last update timestamp. |

## Native endpoint

Through the native Availity API, this operation is `GET /availity/v1/professional-claims/{id}` (base URL `https://api.availity.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-professional-predetermination.md) for the provider-specific parameters and requirements.

