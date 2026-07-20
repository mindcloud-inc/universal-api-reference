# Clappia: Add Field

Creates a new app field in Clappia.

```
POST https://connect.mindcloud.co/v1/universal/clappia/latest/actions/add-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clappia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clappia/latest/actions/add-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string",
  "sectionIndex": 1,
  "fieldIndex": 1,
  "fieldType": "string",
  "label": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clappia/latest/actions/add-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string",
    "sectionIndex": 1,
    "fieldIndex": 1,
    "fieldType": "string",
    "label": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | yes | Clappia app ID. |
| `sectionIndex` | number | yes | Zero-based section index where the field should be inserted. |
| `fieldIndex` | number | yes | Zero-based insertion index for the field inside the section. |
| `fieldType` | string | yes | Clappia field type to create, such as singleSelector. |
| `label` | string | yes | Field label shown to users. |
| `description` | string | no | Optional helper text for the field. |
| `required` | boolean | no | Whether the field must be filled in. |
| `blockWidthPercentageDesktop` | number | no | Desktop width percentage for the field block. |
| `blockWidthPercentageMobile` | number | no | Mobile width percentage for the field block. |
| `options[]` | array<string> | no | Selectable values for option-based field types. |
| `style` | string | no | Display style for supported field types, such as Standard or Chips. |
| `numberOfCols` | number | no | Column count for option display layouts. |
| `isEditable` | boolean | no | Whether users can edit the field. |
| `retainValues` | boolean | no | Whether field values should be retained when relevant form structure changes. |

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

Through the native Clappia API, this operation is `POST /appdefinitionv2/addField` (base URL `https://api-public-v4.clappia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-field.md) for the provider-specific parameters and requirements.

