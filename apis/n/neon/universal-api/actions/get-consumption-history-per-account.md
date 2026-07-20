# Neon: Retrieve account consumption metrics (legacy plans)



```
GET https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-consumption-history-per-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-consumption-history-per-account?connectionId=$CONNECTION_ID&from=2026-05-07T12%3A00%3A00.000Z&to=2026-05-07T12%3A00%3A00.000Z&granularity=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "2026-05-07T12:00:00.000Z",
  "to": "2026-05-07T12:00:00.000Z",
  "granularity": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-consumption-history-per-account?${params}`, {
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
| `from` | date | yes | Neon API parameter from |
| `to` | date | yes | Neon API parameter to |
| `granularity` | list | yes | Neon API parameter granularity One of: `0`, `1`, `2`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `org_id` | string | no | Neon API parameter org_id |
| `include_v1_metrics` | boolean | no | Neon API parameter include_v1_metrics |
| `metrics[]` | array<string> | no | Neon API parameter metrics Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "periods": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `periods` | array<object> |  |

## Native endpoint

Through the native Neon API, this operation is `GET /consumption_history/account` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-consumption-history-per-account.md) for the provider-specific parameters and requirements.

