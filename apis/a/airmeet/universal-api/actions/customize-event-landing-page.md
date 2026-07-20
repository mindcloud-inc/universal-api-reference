# Airmeet: Customize Event Landing Page

Updates an event landing page in Airmeet.

```
PUT https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/customize-event-landing-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airmeet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/customize-event-landing-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "airmeetId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/customize-event-landing-page', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "airmeetId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `airmeetId` | string | yes | The Airmeet event ID. |
| `ambience` | string | no | Landing page theme, LIGHT or DARK. |
| `buttonTextColor` | string | no | Hex color for button text, for example #ff9847. |
| `highlightColor` | string | no | Hex color for highlight elements, for example #0000ff. |
| `imageUrl` | string | no | Public JPG, JPEG, or PNG URL for the landing page hero image. |
| `layout` | string | no | Landing page layout, CLASSIC or MODERN. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Airmeet API returns.

## Native endpoint

Through the native Airmeet API, this operation is `PUT /airmeet/{airmeetId}/landing-page` (base URL `https://api-gateway-prod.us.airmeet.com/prod`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/customize-event-landing-page.md) for the provider-specific parameters and requirements.

