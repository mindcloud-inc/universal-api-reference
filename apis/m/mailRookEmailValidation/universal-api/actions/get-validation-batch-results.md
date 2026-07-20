# MailRook Email Validation: Get Validation Batch Results

Retrieves email validation batch results from MailRook.

```
GET https://connect.mindcloud.co/v1/universal/mailRookEmailValidation/latest/actions/get-validation-batch-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailRook Email Validation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailRookEmailValidation/latest/actions/get-validation-batch-results?connectionId=$CONNECTION_ID&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailRookEmailValidation/latest/actions/get-validation-batch-results?${params}`, {
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
| `listId` | string | yes | MailRook batch list identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": [
        {}
      ],
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | MailRook response code. |
| `data` | array<object> | Validation results for each email in the batch. |
| `message` | string | MailRook response message. |

## Native endpoint

Through the native MailRook Email Validation API, this operation is `GET /validate/list/:listId` (base URL `https://api.mailrook.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-validation-batch-results.md) for the provider-specific parameters and requirements.

