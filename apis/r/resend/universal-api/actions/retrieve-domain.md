# Resend: Retrieve Domain

Retrieves a domain from Resend.

```
GET https://connect.mindcloud.co/v1/universal/resend/latest/actions/retrieve-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Resend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/resend/latest/actions/retrieve-domain?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/resend/latest/actions/retrieve-domain?${params}`, {
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
| `id` | string<string> | yes | The domain ID to retrieve |

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
      "object": "string",
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
| `object` | string | Object type identifier. |
| `openTracking` | boolean | Whether open tracking is enabled. |
| `records` | array<object> | DNS records for verification. |
| `region` | string | Region where the domain is hosted. |
| `status` | string | Current domain status. |
| `trackingSubdomain` | string | Tracking subdomain, when present. |

## Native endpoint

Through the native Resend API, this operation is `GET /domains/:id` (base URL `https://api.resend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-domain.md) for the provider-specific parameters and requirements.

