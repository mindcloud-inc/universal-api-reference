# GoDaddy CRM: Update Privacy Forwarding Settings

Updates privacy forwarding settings for a GoDaddy domain.

```
PUT https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/update-privacy-forwarding-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoDaddy CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/update-privacy-forwarding-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "1234567890",
  "domain": "example.com",
  "privateEmailType": "DEFAULT",
  "emailPreference": "EMAIL_SEND_NONE"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/update-privacy-forwarding-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "1234567890",
    "domain": "example.com",
    "privateEmailType": "DEFAULT",
    "emailPreference": "EMAIL_SEND_NONE"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | string | yes | Required customer identifier who owns the domain Example: `1234567890`. |
| `domain` | string | yes | Required domain whose privacy forwarding should be updated Example: `example.com`. |
| `privateEmailType` | string | yes | Required private email type Default: `DEFAULT`. Example: `DEFAULT`. |
| `emailPreference` | string | yes | Required forwarding preference Default: `EMAIL_SEND_NONE`. Example: `EMAIL_SEND_NONE`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `forwardingEmail` | string | no | Optional forwarding destination email Example: `privacy@example.com`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GoDaddy CRM API returns.

## Native endpoint

Through the native GoDaddy CRM API, this operation is `PATCH /v2/customers/:customerId/domains/:domain/privacy/forwarding` (base URL `https://api.godaddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-privacy-forwarding-settings.md) for the provider-specific parameters and requirements.

