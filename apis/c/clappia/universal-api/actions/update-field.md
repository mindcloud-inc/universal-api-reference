# Clappia: Update Field

Updates an existing app field in Clappia.

```
PUT https://connect.mindcloud.co/v1/universal/clappia/latest/actions/update-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clappia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clappia/latest/actions/update-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string",
  "fieldName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clappia/latest/actions/update-field', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string",
    "fieldName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | yes | Clappia app ID. |
| `fieldName` | string | yes | Current variable name of the field to update. |
| `newFieldName` | string | no | Optional new variable name for the field. |
| `label` | string | no | Updated field label. |
| `description` | string | no | Updated helper text for the field. |
| `required` | boolean | no | Whether the field must be filled in. |
| `blockWidthPercentageDesktop` | number | no | Updated desktop width percentage for the field block. |
| `blockWidthPercentageMobile` | number | no | Updated mobile width percentage for the field block. |
| `validation` | string | no | Updated validation mode for the field. |
| `isEditable` | boolean | no | Whether users can edit the field after the update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fieldName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fieldName` | string |  |

## Native endpoint

Through the native Clappia API, this operation is `POST /appdefinitionv2/updateField` (base URL `https://api-public-v4.clappia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-field.md) for the provider-specific parameters and requirements.

