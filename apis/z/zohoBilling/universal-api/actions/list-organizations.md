# Zoho Billing: List Organizations



```
GET https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/list-organizations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "message": "string",
      "organizations": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `message` | string |  |
| `organizations[]` | array<object> |  |
| `organizations[].contact_name` | string |  |
| `organizations[].country` | string |  |
| `organizations[].country_code` | string |  |
| `organizations[].currency_code` | string |  |
| `organizations[].email` | string |  |
| `organizations[].is_default_org` | boolean |  |
| `organizations[].mode` | string |  |
| `organizations[].name` | string |  |
| `organizations[].organization_id` | string |  |
| `organizations[].plan_name` | string |  |
| `organizations[].time_zone` | string |  |

## Native endpoint

Through the native Zoho Billing API, this operation is `GET /organizations` (base URL `{{credentials.accessTokenRequest.api_domain}}/billing/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

