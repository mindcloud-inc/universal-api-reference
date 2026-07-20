# Qlik: Get App Metadata

Retrieves metadata for an app in Qlik.

```
GET https://connect.mindcloud.co/v1/universal/qlik/latest/actions/get-app-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qlik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qlik/latest/actions/get-app-metadata?connectionId=$CONNECTION_ID&appId=65b8f2a1f4b0c2d3e4f56789" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "65b8f2a1f4b0c2d3e4f56789"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qlik/latest/actions/get-app-metadata?${params}`, {
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
| `appId` | string | yes | Qlik app ID. Example: `65b8f2a1f4b0c2d3e4f56789`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fields": [
        [
          {}
        ]
      ],
      "has_section_access": true,
      "is_direct_query_mode": true,
      "reload_meta": {},
      "static_byte_size": 1,
      "tables": [
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
| `fields[]` | array<object> |  |
| `has_section_access` | boolean |  |
| `is_direct_query_mode` | boolean |  |
| `reload_meta` | object |  |
| `static_byte_size` | number |  |
| `tables[]` | array<object> |  |

## Native endpoint

Through the native Qlik API, this operation is `GET /api/v1/apps/:appId/data/metadata` (base URL `https://{{credentials.tenantHost}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-app-metadata.md) for the provider-specific parameters and requirements.

