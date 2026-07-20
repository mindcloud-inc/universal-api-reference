# Weberlo: Create Form Submit Event

Creates a form submit event in Weberlo.

```
POST https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/create-form-submit-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weberlo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/create-form-submit-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "time": "1712083200000"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/create-form-submit-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "time": "1712083200000"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `time` | number | yes | Event timestamp in milliseconds. Example: `1712083200000`. |
| `email` | string | no | Visitor email address. Example: `wizard-stage3+lead@example.com`. |
| `firstName` | string | no | Visitor first name. Example: `Avery`. |
| `lastName` | string | no | Visitor last name. Example: `Lopez`. |
| `name` | string | no | Visitor full name. Example: `Avery Lopez`. |
| `formType` | string | no | Form type label. Example: `newsletter`. |
| `formId` | string | no | Form identifier. Example: `123e4567-e89b-12d3-a456-426655440003`. |
| `sessionId` | string | no | Session identifier. Example: `123e4567-e89b-12d3-a456-426655440003`. |
| `website` | string | no | Website host or name. Example: `wizard-stage3.example.com`. |
| `href` | string | no | Page URL where the form submit happened. Example: `https://wizard-stage3.example.com/landing`. |
| `device` | string | no | Device type. Example: `mobile`. |
| `country` | string | no | Country code or country value. Example: `US`. |
| `phone` | string | no | Visitor phone number. Example: `928002271555`. |
| `ipAddress` | string | no | Visitor IP address. Example: `1.1.1.1`. |
| `utmSource` | string | no | UTM source. Example: `newsletter`. |
| `utmMedium` | string | no | UTM medium. Example: `email`. |
| `utmCampaign` | string | no | UTM campaign. Example: `spring-launch`. |
| `utmContent` | string | no | UTM content. Example: `hero-cta`. |
| `fbclid` | string | no | Facebook click identifier. Example: `fbclid-value`. |
| `gclid` | string | no | Google click identifier. Example: `gclid-value`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Weberlo API returns.

## Native endpoint

Through the native Weberlo API, this operation is `POST /event/form` (base URL `https://connect.weberlo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-form-submit-event.md) for the provider-specific parameters and requirements.

