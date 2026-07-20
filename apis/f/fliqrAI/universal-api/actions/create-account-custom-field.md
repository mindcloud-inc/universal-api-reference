# Fliqr AI: Create Account Custom Field



```
POST https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/create-account-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fliqr AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/create-account-custom-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/create-account-custom-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Custom field name. |
| `type` | number | no | Custom field type: 0 text, 1 number, 2 date, 3 datetime, 4 boolean. |
| `isBotField` | boolean | no | Whether this is a bot field. |
| `value` | string | no | Bot field value; ignored for user custom fields. |
| `description` | string | no | Custom field description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen"
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

## Native endpoint

Through the native Fliqr AI API, this operation is `POST /accounts/custom_fields` (base URL `https://app.fliqr.ai/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-account-custom-field.md) for the provider-specific parameters and requirements.

