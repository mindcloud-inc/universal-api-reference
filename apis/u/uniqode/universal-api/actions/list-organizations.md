# Uniqode: List Organizations

Retrieves organizations from your Uniqode account.

```
GET https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uniqode `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/list-organizations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/list-organizations?${params}`, {
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
      "count": 1,
      "next": "string",
      "previous": "string",
      "results": [
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `next` | string |  |
| `previous` | string |  |
| `results` | array<object> |  |
| `results[].allow_analytics_export` | boolean |  |
| `results[].check_response_limits` | boolean |  |
| `results[].created` | date |  |
| `results[].email_wallet_pass` | boolean |  |
| `results[].enforce_qr_templates` | boolean |  |
| `results[].form_service` | number |  |
| `results[].id` | number |  |
| `results[].name` | string |  |
| `results[].physical_web_active` | boolean |  |
| `results[].reseller_access` | boolean |  |
| `results[].updated` | date |  |
| `results[].wallet_active` | boolean |  |
| `results[].whitelabel_access` | boolean |  |

## Native endpoint

Through the native Uniqode API, this operation is `GET /organizations/` (base URL `https://api.uniqode.com/api/2.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

