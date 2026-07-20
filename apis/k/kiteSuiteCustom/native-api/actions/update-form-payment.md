# Update Form payment with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/form/payment/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update Form payment](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | yes | ID of the form payment element to update. |
| `title` | body | `string` | yes | Title of the form element. |
| `subTitle` | body | `string` | yes | Subtitle of the form element. |
| `placeholder` | body | `string` | yes | Placeholder text for the form element. |
| `defaultValue` | body | `string` | yes | Default value for the form element. |
| `validationType` | body | `string` | yes | Validation type for the form element. |
| `CharLimit` | body | `number` | yes | Character limit for the form element. |
| `mcqLimit` | body | `number` | yes | MCQ limit for the form element. |
| `currencyType` | body | `string` | yes | Currency type for the form element. |
| `addressLabels` | body | `object` | yes | Address labels for the form element. |
| `options[]` | body | `array` | yes | Options for the form element. |
| `temsConditionText` | body | `string` | yes | Terms and conditions text. |
| `temsConditionLink` | body | `string` | yes | Terms and conditions link. |
| `isRequired` | body | `boolean` | yes | Indicates if the form element is required. |
| `isShrinked` | body | `boolean` | yes | Indicates if the form element is shrinked. |
| `isHidden` | body | `boolean` | yes | Indicates if the form element is hidden. |
| `iconAvatar` | body | `string` | yes | Icon avatar for the form element. |
| `iconAvatarZoom` | body | `number` | yes | Icon avatar zoom level. |
| `verticleAlignment` | body | `string` | yes | Vertical alignment of the form element. |
| `horizontallyAlignment` | body | `string` | yes | Horizontal alignment of the form element. |
| `imageAlignment` | body | `string` | yes | Image alignment of the form element. |
| `isReadOnly` | body | `boolean` | yes | Indicates if the form element is read-only. |
| `HeadingSize` | body | `string` | yes | Heading size for the form element. |
| `labelAlignment` | body | `string` | yes | Label alignment for the form element. |
| `socialLinks` | body | `object` | yes | Social links for the form element. |
| `fileTypeSupport[]` | body | `array` | yes | Supported file types for the form element. |
| `uploadType` | body | `string` | yes | Upload type for the form element. |
| `myProducts` | body | `object` | yes | My products for the form element. |
| `paymentCurrency` | body | `string` | yes | Payment currency for the form element. |
| `paymentType` | body | `string` | yes | Payment type for the form element. |
| `paymentMode` | body | `string` | yes | Payment mode for the form element. |
| `productView` | body | `string` | yes | Product view type for the form element. |
| `shipping` | body | `object` | yes | Shipping information |
| `tax` | body | `object` | yes | Tax information. |
| `isShowSearch` | body | `boolean` | yes | show search box |
| `isShowFilter` | body | `boolean` | yes | show filter box |
| `invoice` | body | `object` | yes | invoice settings. |
| `defaultDiscount` | body | `number` | yes | default discount percentage |
