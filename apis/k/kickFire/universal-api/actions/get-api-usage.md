# KickFire: Get API Usage

Retrieves API usage information from KickFire.

```
GET https://connect.mindcloud.co/v1/universal/kickFire/latest/actions/get-api-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KickFire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kickFire/latest/actions/get-api-usage?connectionId=$CONNECTION_ID&edate=2026-04-02&sdate=2026-04-01" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "edate": "2026-04-02",
  "sdate": "2026-04-01"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kickFire/latest/actions/get-api-usage?${params}`, {
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
| `edate` | string | yes | Inclusive usage report end date in YYYY-MM-DD format. Example: `2026-04-02`. |
| `sdate` | string | yes | Inclusive usage report start date in YYYY-MM-DD format. Example: `2026-04-01`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        [
          {}
        ]
      ],
      "endpoint": "string",
      "endpointName": "Ava Chen",
      "status": "string",
      "totalQueries": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | array<object> |  |
| `data[].dailyQueries` | string |  |
| `data[].queryDate` | string |  |
| `endpoint` | string |  |
| `endpointName` | string |  |
| `status` | string |  |
| `totalQueries` | string |  |

## Native endpoint

Through the native KickFire API, this operation is `GET /usage` (base URL `https://api.kickfire.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-usage.md) for the provider-specific parameters and requirements.

