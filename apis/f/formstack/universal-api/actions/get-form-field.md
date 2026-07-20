# Formstack: Get Form Field

Retrieves a field from a Formstack form.

```
GET https://connect.mindcloud.co/v1/universal/formstack/latest/actions/get-form-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formstack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formstack/latest/actions/get-form-field?connectionId=$CONNECTION_ID&formId=6457226&fieldId=193364423" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "6457226",
  "fieldId": "193364423"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formstack/latest/actions/get-form-field?${params}`, {
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
| `formId` | number | yes | The ID of the form. Example: `6457226`. |
| `fieldId` | number | yes | The ID of the field. Example: `193364423`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "confirmationText": "string",
        "hideInputCharacters": true,
        "maxLength": 1,
        "minLength": 1,
        "placeholder": "string",
        "removeDataFromEmailsAndExports": true,
        "requireConfirmation": true,
        "restrictDataAccess": true
      },
      "columnSpan": 1,
      "defaultValue": "string",
      "displayOrder": 1,
      "hidden": true,
      "hideLabel": true,
      "id": 1,
      "label": "string",
      "labelKey": "string",
      "language": "string",
      "readOnly": true,
      "required": true,
      "supportingText": "string",
      "type": "string",
      "unique": true,
      "useCallout": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.confirmationText` | string |  |
| `attributes.hideInputCharacters` | boolean |  |
| `attributes.maxLength` | number |  |
| `attributes.minLength` | number |  |
| `attributes.placeholder` | string |  |
| `attributes.removeDataFromEmailsAndExports` | boolean |  |
| `attributes.requireConfirmation` | boolean |  |
| `attributes.restrictDataAccess` | boolean |  |
| `columnSpan` | number |  |
| `defaultValue` | string |  |
| `displayOrder` | number |  |
| `hidden` | boolean |  |
| `hideLabel` | boolean |  |
| `id` | number |  |
| `label` | string |  |
| `labelKey` | string |  |
| `language` | string |  |
| `readOnly` | boolean |  |
| `required` | boolean |  |
| `supportingText` | string |  |
| `type` | string |  |
| `unique` | boolean |  |
| `useCallout` | boolean |  |

## Native endpoint

Through the native Formstack API, this operation is `GET /forms/:formId/fields/:fieldId` (base URL `https://www.formstack.com/api/v2025`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-field.md) for the provider-specific parameters and requirements.

