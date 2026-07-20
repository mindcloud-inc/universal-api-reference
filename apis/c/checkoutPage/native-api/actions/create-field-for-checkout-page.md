# Create Field For Checkout Page with Checkout Page

Creates a field for a checkout page in Checkout Page.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/checkout-pages/:pageId/fields`
- **Base URL:** `https://api.checkoutpage.com`
- **Official documentation:** [Create Field For Checkout Page](https://checkoutpage.com/docs/api/v1/checkout-pages/fields/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageId` | path | `string` | yes | Unique identifier. Must be in BSON ObjectId format. |
| `label` | body | `string` | yes | Form label for the input element. |
| `type` | body | `string` | no | Used to store field data in a predictable manner. Please note that you must use Customer Name and Shipping Address if you wish to use any of the shipping address data types. |
| `placeholder` | body | `string` | no | Specifies a short hint that describes the expected value of an input element |
| `element` | body | `string` | no | Input control used to render this field in checkout. Defaults to `text`. |
| `options[]` | body | `array<object>` | no | Selectable options. Applies to `select` and `multiple-choice` elements. |
| `required` | body | `boolean` | no | Whether this field must be completed before checkout can continue. |
| `reference` | body | `string` | no | External reference ID for integration purposes. |
| `hidden` | body | `boolean` | no | Whether this field is hidden from customers at checkout. |
| `defaultValue` | body | `object` | no | Default value settings for the field. |
| `showHideLogic` | body | `object` | no | Conditional visibility rules for this field. |
| `minValue` | body | `object` | no | Minimum allowed value settings for this field. |
| `maxValue` | body | `object` | no | Maximum allowed value settings for this field. |
