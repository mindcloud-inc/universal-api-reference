# Listrak Email: Send Transactional Email



```
POST https://connect.mindcloud.co/v1/universal/listrakEmail/latest/actions/send-transactional-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Listrak Email `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/listrakEmail/latest/actions/send-transactional-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": 1,
  "transactionalMessageId": 1,
  "emailAddress": "customer@example.com",
  "segmentationFieldValues[]": "[object Object]",
  "segmentationFieldValues[].segmentationFieldId": 1,
  "segmentationFieldValues[].value": "1004827"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/listrakEmail/latest/actions/send-transactional-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": 1,
    "transactionalMessageId": 1,
    "emailAddress": "customer@example.com",
    "segmentationFieldValues[]": "[object Object]",
    "segmentationFieldValues[].segmentationFieldId": 1,
    "segmentationFieldValues[].value": "1004827"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listId` | number | yes | Identifier used to locate the Listrak list. |
| `transactionalMessageId` | number | yes | Identifier used to locate the previously-created transactional message/template. |
| `emailAddress` | string | yes | Email address of the contact to send to. Example: `customer@example.com`. |
| `segmentationFieldValues[]` | array<object> | yes | Array of profile field values used to populate dynamic placeholders in the transactional email template. Each item should include `segmentationFieldId` and `value`. Example: `[object Object]`. |
| `segmentationFieldValues[].segmentationFieldId` | number | yes | Numeric API ID of the Listrak profile field used as a template placeholder. |
| `segmentationFieldValues[].value` | string | yes | Value to populate for this profile field in the transactional email template. Example: `1004827`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "resourceId": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `resourceId` | string | Identifier used to locate the created send resource. |
| `status` | number | HTTP status code returned by Listrak. |

## Native endpoint

Through the native Listrak Email API, this operation is `POST /v1/List/:listId/TransactionalMessage/:transactionalMessageId/Message` (base URL `https://api.listrak.com/email`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-transactional-email.md) for the provider-specific parameters and requirements.

