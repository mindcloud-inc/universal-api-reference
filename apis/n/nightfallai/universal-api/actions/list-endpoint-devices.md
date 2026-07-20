# Nightfall.ai: List Endpoint Devices

Retrieves endpoint devices from Nightfall.ai.

```
GET https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/list-endpoint-devices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nightfall.ai `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/list-endpoint-devices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/list-endpoint-devices?${params}`, {
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
| `query` | string | no | Optional free-text search across endpoint devices. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agents": [
        {}
      ],
      "totalAgents": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agents` | array<object> | Endpoint device records available to Nightfall. |
| `totalAgents` | number | Total number of endpoint device records. |

## Native endpoint

Through the native Nightfall.ai API, this operation is `GET /apps/v1/endpoint/devices` (base URL `https://api.nightfall.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-endpoint-devices.md) for the provider-specific parameters and requirements.

