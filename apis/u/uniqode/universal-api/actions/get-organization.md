# Uniqode: Get Organization

Retrieves an organization from your Uniqode account.

```
GET https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uniqode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/get-organization?connectionId=$CONNECTION_ID&organizationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/get-organization?${params}`, {
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
| `organizationId` | number | yes | The Uniqode organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allow_analytics_export": true,
      "check_response_limits": true,
      "created": "2026-05-07T12:00:00.000Z",
      "email_wallet_pass": true,
      "enforce_qr_templates": true,
      "form_service": 1,
      "id": 1,
      "name": "Ava Chen",
      "physical_web_active": true,
      "reseller_access": true,
      "updated": "2026-05-07T12:00:00.000Z",
      "wallet_active": true,
      "whitelabel_access": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allow_analytics_export` | boolean |  |
| `check_response_limits` | boolean |  |
| `created` | date |  |
| `email_wallet_pass` | boolean |  |
| `enforce_qr_templates` | boolean |  |
| `form_service` | number |  |
| `id` | number |  |
| `name` | string |  |
| `physical_web_active` | boolean |  |
| `reseller_access` | boolean |  |
| `updated` | date |  |
| `wallet_active` | boolean |  |
| `whitelabel_access` | boolean |  |

## Native endpoint

Through the native Uniqode API, this operation is `GET /organizations/:organizationId/` (base URL `https://api.uniqode.com/api/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

