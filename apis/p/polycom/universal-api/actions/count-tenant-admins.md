# Polycom: Count Tenant Admins

Counts admin users in a selected Poly Lens tenant.

```
GET https://connect.mindcloud.co/v1/universal/polycom/latest/actions/count-tenant-admins
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Polycom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/polycom/latest/actions/count-tenant-admins?connectionId=$CONNECTION_ID&variables.params.grants%5B0%5D.resourceId=500c2d28-df9c-491a-84d7-a02ff4b2036d" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.params.grants[0].resourceId": "500c2d28-df9c-491a-84d7-a02ff4b2036d"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/polycom/latest/actions/count-tenant-admins?${params}`, {
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
| `variables.params.grants[0].resourceId` | string | yes | The Poly Lens tenant ID to scope the admin user count. Example: `500c2d28-df9c-491a-84d7-a02ff4b2036d`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |

## Native endpoint

Through the native Polycom API, this operation is `POST /graphql` (base URL `https://api.silica-prod01.io.lens.poly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/count-tenant-admins.md) for the provider-specific parameters and requirements.

