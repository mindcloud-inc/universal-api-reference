# Iris Dfir: List Assets



```
GET https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/list-assets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Iris Dfir `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/list-assets?connectionId=$CONNECTION_ID&limit=25&offset=0&caseIdentifier=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "caseIdentifier": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/list-assets?${params}`, {
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
| `caseIdentifier` | number | yes | IRIS case identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alerts": [
        {}
      ],
      "analysis_status": {},
      "analysis_status_id": 1,
      "asset_compromise_status_id": 1,
      "asset_description": "string",
      "asset_domain": "string",
      "asset_enrichment": "string",
      "asset_id": 1,
      "asset_info": "string",
      "asset_ip": "string",
      "asset_name": "Ava Chen",
      "asset_tags": "string",
      "asset_type_id": 1,
      "asset_type": {
        "asset_description": "string",
        "asset_icon_compromised": "string",
        "asset_icon_not_compromised": "string",
        "asset_id": 1,
        "asset_name": "Ava Chen"
      },
      "asset_uuid": "string",
      "case_id": 1,
      "custom_attributes": {},
      "date_added": "2026-05-07T12:00:00.000Z",
      "date_update": "2026-05-07T12:00:00.000Z",
      "modification_history": {},
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alerts` | array<object> |  |
| `analysis_status` | object |  |
| `analysis_status_id` | number |  |
| `asset_compromise_status_id` | number |  |
| `asset_description` | string |  |
| `asset_domain` | string |  |
| `asset_enrichment` | string |  |
| `asset_id` | number |  |
| `asset_info` | string |  |
| `asset_ip` | string |  |
| `asset_name` | string |  |
| `asset_tags` | string |  |
| `asset_type_id` | number |  |
| `asset_type.asset_description` | string |  |
| `asset_type.asset_icon_compromised` | string |  |
| `asset_type.asset_icon_not_compromised` | string |  |
| `asset_type.asset_id` | number |  |
| `asset_type.asset_name` | string |  |
| `asset_uuid` | string |  |
| `case_id` | number |  |
| `custom_attributes` | object |  |
| `date_added` | date |  |
| `date_update` | date |  |
| `modification_history` | object |  |
| `user_id` | number |  |

## Native endpoint

Through the native Iris Dfir API, this operation is `GET /api/v2/cases/:case_identifier/assets` (base URL `https://v200.beta.dfir-iris.org`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-assets.md) for the provider-specific parameters and requirements.

