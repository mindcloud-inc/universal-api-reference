# Statsig: List Dynamic Configs

Retrieves dynamic configs from Statsig.

```
GET https://connect.mindcloud.co/v1/universal/statsig/latest/actions/list-dynamic-configs-get-console-v1-dynamic-configs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/list-dynamic-configs-get-console-v1-dynamic-configs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statsig/latest/actions/list-dynamic-configs-get-console-v1-dynamic-configs?${params}`, {
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
| `releasePipelineID` | string | no | The release pipeline ID associated with the dynamic config |
| `teamID` | string | no | Filter by team ID |
| `targetAppID` | string | no | Filter by target app ID |
| `creatorName` | string | no | Name of the creator. |
| `creatorID` | string | no | ID of the user who created the entity. |
| `tags` | string | no | Filter by tags |
| `limit` | number | no | Results per page |
| `page` | number | no | Page number |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Statsig response data payload. |
| `message` | string | Statsig response message. |

## Native endpoint

Through the native Statsig API, this operation is `GET /console/v1/dynamic_configs` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-dynamic-configs-get-console-v1-dynamic-configs.md) for the provider-specific parameters and requirements.

