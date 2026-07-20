# Ortto: Update Account Custom Field



```
PUT https://connect.mindcloud.co/v1/universal/ortto/latest/actions/update-account-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ortto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ortto/latest/actions/update-account-custom-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fieldId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ortto/latest/actions/update-account-custom-field', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fieldId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fieldId` | string | yes | Ortto custom field identifier such as str:o:favorite-color. |
| `replace_values[]` | array<string> | no | Replace the full option list for this select-style field. Accepts multiple values as an array. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `add_values[]` | array<string> | no | Append new options for this select-style field. Accepts multiple values as an array. |
| `remove_values[]` | array<string> | no | Remove existing options from this select-style field. Accepts multiple values as an array. |
| `trackChanges` | boolean | no | Whether Ortto should retain change history for this field. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fieldId": "string",
      "trackChanges": true,
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
| `fieldId` | string |  |
| `trackChanges` | boolean |  |
| `values[]` | string |  |

## Native endpoint

Through the native Ortto API, this operation is `PUT /organizations/custom-field/update` (base URL `{{credentials.apiBaseUrl}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-account-custom-field.md) for the provider-specific parameters and requirements.

