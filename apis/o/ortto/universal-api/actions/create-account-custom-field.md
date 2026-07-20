# Ortto: Create Account Custom Field



```
POST https://connect.mindcloud.co/v1/universal/ortto/latest/actions/create-account-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ortto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ortto/latest/actions/create-account-custom-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ortto/latest/actions/create-account-custom-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | Ortto custom field type such as text, integer, or single_select. |
| `name` | string | yes | Internal custom field name. Ortto requires this and does not accept display_name for creation. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `values[]` | array<string> | no | Option values for select-style custom fields. Accepts multiple values as an array. |
| `trackChanges` | boolean | no | Whether Ortto should retain change history for this field. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayType": "string",
      "fieldId": "string",
      "name": "Ava Chen",
      "values": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayType` | string |  |
| `fieldId` | string |  |
| `name` | string |  |
| `values[]` | string |  |

## Native endpoint

Through the native Ortto API, this operation is `POST /accounts/custom-field/create` (base URL `{{credentials.apiBaseUrl}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-account-custom-field.md) for the provider-specific parameters and requirements.

