# Kite Suite: Update Form payment



```
PUT https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-form-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-form-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "id": "string",
  "title": "string",
  "subTitle": "string",
  "placeholder": "string",
  "defaultValue": "string",
  "validationType": "string",
  "CharLimit": 1,
  "mcqLimit": 1,
  "currencyType": "string",
  "addressLabels": {},
  "options[]": [
    "string"
  ],
  "temsConditionText": "string",
  "temsConditionLink": "https://example.com",
  "isRequired": true,
  "isShrinked": true,
  "isHidden": true,
  "iconAvatar": "string",
  "iconAvatarZoom": 1,
  "verticleAlignment": "string",
  "horizontallyAlignment": "string",
  "imageAlignment": "string",
  "isReadOnly": true,
  "HeadingSize": "string",
  "labelAlignment": "string",
  "socialLinks": {},
  "fileTypeSupport[]": [
    "string"
  ],
  "uploadType": "string",
  "myProducts": {},
  "paymentCurrency": "string",
  "paymentType": "string",
  "paymentMode": "string",
  "productView": "string",
  "shipping": {},
  "tax": {},
  "isShowSearch": true,
  "isShowFilter": true,
  "invoice": {},
  "defaultDiscount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-form-payment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "id": "string",
    "title": "string",
    "subTitle": "string",
    "placeholder": "string",
    "defaultValue": "string",
    "validationType": "string",
    "CharLimit": 1,
    "mcqLimit": 1,
    "currencyType": "string",
    "addressLabels": {},
    "options[]": ["string"],
    "temsConditionText": "string",
    "temsConditionLink": "https://example.com",
    "isRequired": true,
    "isShrinked": true,
    "isHidden": true,
    "iconAvatar": "string",
    "iconAvatarZoom": 1,
    "verticleAlignment": "string",
    "horizontallyAlignment": "string",
    "imageAlignment": "string",
    "isReadOnly": true,
    "HeadingSize": "string",
    "labelAlignment": "string",
    "socialLinks": {},
    "fileTypeSupport[]": ["string"],
    "uploadType": "string",
    "myProducts": {},
    "paymentCurrency": "string",
    "paymentType": "string",
    "paymentMode": "string",
    "productView": "string",
    "shipping": {},
    "tax": {},
    "isShowSearch": true,
    "isShowFilter": true,
    "invoice": {},
    "defaultDiscount": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Request body |
| `id` | string | yes | ID of the form payment element to update. |
| `title` | string | yes | Title of the form element. |
| `subTitle` | string | yes | Subtitle of the form element. |
| `placeholder` | string | yes | Placeholder text for the form element. |
| `defaultValue` | string | yes | Default value for the form element. |
| `validationType` | string | yes | Validation type for the form element. |
| `CharLimit` | number | yes | Character limit for the form element. |
| `mcqLimit` | number | yes | MCQ limit for the form element. |
| `currencyType` | string | yes | Currency type for the form element. |
| `addressLabels` | object | yes | Address labels for the form element. |
| `options[]` | array | yes | Options for the form element. |
| `temsConditionText` | string | yes | Terms and conditions text. |
| `temsConditionLink` | string | yes | Terms and conditions link. |
| `isRequired` | boolean | yes | Indicates if the form element is required. |
| `isShrinked` | boolean | yes | Indicates if the form element is shrinked. |
| `isHidden` | boolean | yes | Indicates if the form element is hidden. |
| `iconAvatar` | string | yes | Icon avatar for the form element. |
| `iconAvatarZoom` | number | yes | Icon avatar zoom level. |
| `verticleAlignment` | string | yes | Vertical alignment of the form element. |
| `horizontallyAlignment` | string | yes | Horizontal alignment of the form element. |
| `imageAlignment` | string | yes | Image alignment of the form element. |
| `isReadOnly` | boolean | yes | Indicates if the form element is read-only. |
| `HeadingSize` | string | yes | Heading size for the form element. |
| `labelAlignment` | string | yes | Label alignment for the form element. |
| `socialLinks` | object | yes | Social links for the form element. |
| `fileTypeSupport[]` | array | yes | Supported file types for the form element. |
| `uploadType` | string | yes | Upload type for the form element. |
| `myProducts` | object | yes | My products for the form element. |
| `paymentCurrency` | string | yes | Payment currency for the form element. |
| `paymentType` | string | yes | Payment type for the form element. |
| `paymentMode` | string | yes | Payment mode for the form element. |
| `productView` | string | yes | Product view type for the form element. |
| `shipping` | object | yes | Shipping information |
| `tax` | object | yes | Tax information. |
| `isShowSearch` | boolean | yes | show search box |
| `isShowFilter` | boolean | yes | show filter box |
| `invoice` | object | yes | invoice settings. |
| `defaultDiscount` | number | yes | default discount percentage |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | object | Updated form element object. |

## Native endpoint

Through the native Kite Suite API, this operation is `PATCH /api/v1/form/payment/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-form-payment.md) for the provider-specific parameters and requirements.

