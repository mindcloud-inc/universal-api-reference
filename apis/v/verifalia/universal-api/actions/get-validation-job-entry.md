# Verifalia: Get Validation Job Entry

Retrieves an entry from an email validation job in Verifalia.

```
GET https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/get-validation-job-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verifalia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/get-validation-job-entry?connectionId=$CONNECTION_ID&id=string&index=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "index": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/get-validation-job-entry?${params}`, {
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
| `id` | string | yes | The Verifalia validation job ID. |
| `index` | number | yes | The zero-based index of the validation entry to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "classification": "string",
      "completedOn": "string",
      "emailAddress": "ava@example.com",
      "index": 1,
      "inputData": "string",
      "isDisposableEmailAddress": true,
      "isFreeEmailAddress": true,
      "isRoleAccount": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `classification` | string | The validation classification such as Deliverable or Undeliverable. |
| `completedOn` | string | When Verifalia completed validation for the entry. |
| `emailAddress` | string | The normalized email address when recognized. |
| `index` | number | The zero-based entry index. |
| `inputData` | string | The original email input submitted to Verifalia. |
| `isDisposableEmailAddress` | boolean | Whether the address is considered disposable. |
| `isFreeEmailAddress` | boolean | Whether the address belongs to a free email provider. |
| `isRoleAccount` | boolean | Whether the address appears to be a role account. |
| `status` | string | The validation status code. |

## Native endpoint

Through the native Verifalia API, this operation is `GET /email-validations/{id}/entries/{index}` (base URL `https://api-1.verifalia.com/v2.7`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-validation-job-entry.md) for the provider-specific parameters and requirements.

