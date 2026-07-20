# Checkout Page: List Fields For Form

Retrieves fields for a form in Checkout Page.

```
GET https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/list-fields-for-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkout Page `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/list-fields-for-form?connectionId=$CONNECTION_ID&pageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/list-fields-for-form?${params}`, {
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
| `pageId` | string | yes | Unique identifier. Must be in BSON ObjectId format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "defaultValue": {},
      "element": "string",
      "hidden": true,
      "id": "string",
      "label": "string",
      "limitAllowedCountries": {},
      "maxValue": {},
      "minValue": {},
      "options": [
        {}
      ],
      "order": 1,
      "placeholder": "string",
      "reference": "string",
      "required": true,
      "showHideLogic": {},
      "showSelectedDialCode": true,
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | ISO-8601 timestamp for when the field was created. |
| `defaultValue` | object | Default value settings for the field. |
| `element` | string | Input control used to render this field at checkout. |
| `hidden` | boolean | Whether this field is hidden from customers at checkout. |
| `id` | string | Unique identifier for the field. |
| `label` | string | Display label shown to customers for this field. |
| `limitAllowedCountries` | object | Country restriction settings for fields that collect country data. |
| `maxValue` | object | Maximum allowed value rules for this field. |
| `minValue` | object | Minimum allowed value rules for this field. |
| `options` | array<object> | Selectable options. Applies to `select` and `multiple-choice` elements. |
| `order` | number | Display order of the field within the form. |
| `placeholder` | string | Placeholder hint shown inside the input before a value is entered. |
| `reference` | string | External reference ID for mapping this field in downstream systems. |
| `required` | boolean | Whether this field must be completed before checkout can continue. |
| `showHideLogic` | object | Conditional visibility rules for this field. |
| `showSelectedDialCode` | boolean | Whether to display the selected international dial code in phone inputs. |
| `type` | string | Used to store field data in a predictable manner. Please note that you must use Customer Name and Shipping Address if you wish to use any of the shipping address data types. |
| `updatedAt` | string | ISO-8601 timestamp for when the field was last updated. |

## Native endpoint

Through the native Checkout Page API, this operation is `GET /v1/forms/:pageId/fields` (base URL `https://api.checkoutpage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fields-for-form.md) for the provider-specific parameters and requirements.

