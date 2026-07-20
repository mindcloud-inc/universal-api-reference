# Peggy Pay: Get Submission by Hash

Retrieves a submission from Peggy Pay by submission hash.

```
GET https://connect.mindcloud.co/v1/universal/peggyPay/latest/actions/get-submission-by-hash
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Peggy Pay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peggyPay/latest/actions/get-submission-by-hash?connectionId=$CONNECTION_ID&hash=abc123submissionhash" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hash": "abc123submissionhash"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peggyPay/latest/actions/get-submission-by-hash?${params}`, {
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
| `hash` | string | yes | Submission hash (`peggyHash`) from a Peggy Pay redirect or webhook. Example: `abc123submissionhash`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "DateAdded": "2026-05-07T12:00:00.000Z",
      "FormKey": "string",
      "Items": {},
      "PaymentAmount": 1,
      "PaymentStatus": "string",
      "Upsells": [
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
| `DateAdded` | date | Submission creation date returned by Peggy Pay. |
| `FormKey` | string | Peggy Pay form key for the submission. |
| `Items` | object | Submitted field items keyed by field name. |
| `PaymentAmount` | number | Payment amount returned by Peggy Pay. |
| `PaymentStatus` | string | Payment status such as complete, init, or error. |
| `Upsells` | array<object> | Upsell records associated with the submission. |

## Native endpoint

Through the native Peggy Pay API, this operation is `GET Formbuilder.Submissions.getSubmissionByHash` (base URL `https://www.peggypay.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-submission-by-hash.md) for the provider-specific parameters and requirements.

