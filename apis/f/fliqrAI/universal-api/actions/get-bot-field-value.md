# Fliqr AI: Get Bot Field Value



```
GET https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/get-bot-field-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fliqr AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/get-bot-field-value?connectionId=$CONNECTION_ID&botFieldId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "botFieldId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/get-bot-field-value?${params}`, {
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
| `botFieldId` | number | yes | Bot field ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "type": 1,
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `type` | number |  |
| `value` | string |  |

## Native endpoint

Through the native Fliqr AI API, this operation is `GET /accounts/bot_fields/:bot_field_id` (base URL `https://app.fliqr.ai/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bot-field-value.md) for the provider-specific parameters and requirements.

