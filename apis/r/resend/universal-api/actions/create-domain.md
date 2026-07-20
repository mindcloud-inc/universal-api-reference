# Resend: Create Domain

Creates a new domain in Resend.

```
POST https://connect.mindcloud.co/v1/universal/resend/latest/actions/create-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Resend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/resend/latest/actions/create-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/resend/latest/actions/create-domain', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `capabilities.sending` | string | no | Default: `enabled`. |
| `name` | string | yes | The name of the domain you want to create. |
| `capabilities.receiving` | string | no | Default: `enabled`. |
| `region` | string | no | Region where emails will be sent from. Possible values: us-east-1, eu-west-1, sa-east-1, ap-northeast-1. Default: `us-east-1`. |
| `customReturnPath` | string | no | Subdomain used for Return-Path address (SPF/DMARC/bounces). Defaults to send. Default: `send`. |
| `openTracking` | boolean | no | Track the open rate of each email. |
| `clickTracking` | boolean | no | Track clicks within each HTML email. |
| `tls` | string | no | TLS mode. Possible values: opportunistic or enforced. Default: `opportunistic`. |
| `capabilities` | object | no | Domain capabilities object. Include sending (enabled\|disabled) and receiving (enabled\|disabled). At least one capability should be enabled. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "capabilities": {},
      "clickTracking": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "openTracking": true,
      "records": [
        {}
      ],
      "region": "string",
      "status": "string",
      "trackingSubdomain": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capabilities` | object | Sending and receiving capabilities. |
| `clickTracking` | boolean | Whether click tracking is enabled. |
| `createdAt` | date | When the domain was created. |
| `id` | string | Domain identifier. |
| `name` | string | Domain name. |
| `openTracking` | boolean | Whether open tracking is enabled. |
| `records` | array<object> | DNS records required for verification. |
| `region` | string | Region where the domain is hosted. |
| `status` | string | Current domain status. |
| `trackingSubdomain` | string | Tracking subdomain, when present. |

## Native endpoint

Through the native Resend API, this operation is `POST /domains` (base URL `https://api.resend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-domain.md) for the provider-specific parameters and requirements.

