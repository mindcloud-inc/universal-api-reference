# Middesk: Fetch guest dashboard link for a registration request

Retrieves a guest dashboard link from Middesk.

```
GET https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-registration-request-guest-dashboard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Middesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-registration-request-guest-dashboard?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-registration-request-guest-dashboard?${params}`, {
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
| `id` | string | yes | ID of the registration request whose guest dashboard you want to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "guestDashboardUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `guestDashboardUrl` | string |  |

## Native endpoint

Through the native Middesk API, this operation is `GET /partner/registration_requests/:id/guest_dashboard` (base URL `https://api.middesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-registration-request-guest-dashboard.md) for the provider-specific parameters and requirements.

