# Kite Suite: Update Form Thank You Page



```
PUT https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-form-thank-you-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-form-thank-you-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "body": {},
  "button": {},
  "logo": "string",
  "logoZoom": 1,
  "text": "string",
  "buttonAlignment": "string",
  "nextSubmission": true,
  "layoutDirection": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-form-thank-you-page', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "body": {},
    "button": {},
    "logo": "string",
    "logoZoom": 1,
    "text": "string",
    "buttonAlignment": "string",
    "nextSubmission": true,
    "layoutDirection": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Form Thank You Page ID |
| `body` | object | yes | Request body |
| `button` | object | yes |  |
| `logo` | string | yes | URL or ID of the logo image |
| `logoZoom` | number | yes | Zoom level for the logo |
| `text` | string | yes | Thank you message text |
| `buttonAlignment` | string | yes | Alignment of the button |
| `nextSubmission` | boolean | yes | Whether to allow next submission |
| `layoutDirection` | string | yes | Direction of the layout |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Kite Suite API returns.

## Native endpoint

Through the native Kite Suite API, this operation is `PATCH /api/v1/form-ty/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-form-thank-you-page.md) for the provider-specific parameters and requirements.

