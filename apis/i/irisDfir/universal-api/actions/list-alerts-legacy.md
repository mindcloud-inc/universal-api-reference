# Iris Dfir: List Alerts Legacy



```
GET https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/list-alerts-legacy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Iris Dfir `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/list-alerts-legacy?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/list-alerts-legacy?${params}`, {
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
      "alert_assets": [
        {}
      ],
      "alert_classification_id": 1,
      "alert_customer_id": 1,
      "alert_description": "string",
      "alert_id": 1,
      "alert_iocs": [
        {}
      ],
      "alert_severity_id": 1,
      "alert_source": "string",
      "alert_source_content": {},
      "alert_source_link": "https://example.com",
      "alert_source_ref": "string",
      "alert_status_id": 1,
      "alert_tags": "string",
      "alert_title": "string",
      "alert_uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alert_assets` | array<object> |  |
| `alert_classification_id` | number |  |
| `alert_customer_id` | number |  |
| `alert_description` | string |  |
| `alert_id` | number |  |
| `alert_iocs` | array<object> |  |
| `alert_severity_id` | number |  |
| `alert_source` | string |  |
| `alert_source_content` | object |  |
| `alert_source_link` | string |  |
| `alert_source_ref` | string |  |
| `alert_status_id` | number |  |
| `alert_tags` | string |  |
| `alert_title` | string |  |
| `alert_uuid` | string |  |

## Native endpoint

Through the native Iris Dfir API, this operation is `GET /alerts/filter` (base URL `https://v200.beta.dfir-iris.org`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-alerts-legacy.md) for the provider-specific parameters and requirements.

