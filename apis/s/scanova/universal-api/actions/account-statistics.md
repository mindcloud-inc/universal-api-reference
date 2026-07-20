# Scanova: Account Statistics



```
GET https://connect.mindcloud.co/v1/universal/scanova/latest/actions/account-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scanova `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scanova/latest/actions/account-statistics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scanova/latest/actions/account-statistics?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | string | no | Comma-separated list of fields to include in the response. If not specified, all fields are returned. Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "custom_domain_count": 1,
      "dynamic_qr_count": 1,
      "lead_list_count": 1,
      "shared_user_count": 1,
      "static_qr_count": 1,
      "total_designer_qr_count": 1,
      "total_qr_count": 1,
      "total_scan_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `custom_domain_count` | number |  |
| `dynamic_qr_count` | number |  |
| `lead_list_count` | number |  |
| `shared_user_count` | number |  |
| `static_qr_count` | number |  |
| `total_designer_qr_count` | number |  |
| `total_qr_count` | number |  |
| `total_scan_count` | number |  |

## Native endpoint

Through the native Scanova API, this operation is `GET /auth/stats/` (base URL `https://management.scanova.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/account-statistics.md) for the provider-specific parameters and requirements.

