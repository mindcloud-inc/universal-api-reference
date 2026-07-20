# Fliqr AI: Set Bot Field Value



```
PUT https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/set-bot-field-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fliqr AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/set-bot-field-value" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "botFieldId": 1,
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/set-bot-field-value', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "botFieldId": 1,
    "value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botFieldId` | number | yes | Bot field ID. |
| `value` | string | yes | Value to set for the bot field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Fliqr AI API, this operation is `POST /accounts/bot_fields/:bot_field_id` (base URL `https://app.fliqr.ai/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-bot-field-value.md) for the provider-specific parameters and requirements.

