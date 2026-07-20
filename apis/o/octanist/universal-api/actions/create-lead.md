# Octanist: Create Lead

Creates a new lead in Octanist.

```
POST https://connect.mindcloud.co/v1/universal/octanist/latest/actions/create-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Octanist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/octanist/latest/actions/create-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/octanist/latest/actions/create-lead', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Lead name. Example: `John Doe`. |
| `email` | string | no | Lead email. Example: `john@example.com`. |
| `phone` | string | no | Lead phone number. Example: `+15551234567`. |
| `custom` | string | no | Custom lead data. Accepts a string or JSON value. Example: `[object Object]`. |
| `note` | string | no | Note to attach to the lead. |
| `website` | string | no | Lead website URL. Example: `https://example.com`. |
| `path` | string | no | Page path associated with the lead. Example: `/contact`. |
| `gclid` | string | no | Google Ads click ID. |
| `fbc` | string | no | Meta click ID. |
| `fbp` | string | no | Meta browser ID. |
| `ga4cid` | string | no | Google Analytics 4 client ID. |
| `ga4sid` | string | no | Google Analytics 4 session ID. |
| `utmSource` | string | no | UTM source value. Example: `google`. |
| `utmMedium` | string | no | UTM medium value. Example: `cpc`. |
| `utmCampaign` | string | no | UTM campaign value. Example: `spring_launch`. |
| `adStorage` | boolean | no | Ad storage consent flag. Default: `false`. |
| `adUserData` | boolean | no | Ad user data consent flag. Default: `false`. |
| `adPersonalization` | boolean | no | Ad personalization consent flag. Default: `false`. |
| `analyticsStorage` | boolean | no | Analytics storage consent flag. Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Octanist API returns.

## Native endpoint

Through the native Octanist API, this operation is `POST /leads` (base URL `https://octanist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lead.md) for the provider-specific parameters and requirements.

