# NextDNS: Get Logs

Retrieves DNS logs from a NextDNS profile.

```
GET https://connect.mindcloud.co/v1/universal/nextDNS/latest/actions/get-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NextDNS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextDNS/latest/actions/get-logs?connectionId=$CONNECTION_ID&limit=25&offset=0&profileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "profileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nextDNS/latest/actions/get-logs?${params}`, {
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
| `profileId` | string | yes | NextDNS profile ID. Defaults to the profile ID stored on the connection when available. |
| `from` | date | no | Filter out logs with older date, inclusive. Example: `-1d`. |
| `to` | date | no | Filter out logs with newer or equal date, exclusive. Example: `2026-04-15T00:00:00Z`. |
| `sort` | string | no | Sort logs from oldest to newest or newest to oldest. Example: `desc`. |
| `limit` | number | no | Limit the number of results returned. Example: `100`. |
| `cursor` | string | no | Use the pagination cursor returned by the previous response. Example: `64v32d9r6rwkcctg6cu38e9g60`. |
| `device` | string | no | Only get logs made for a specific device. Example: `__UNIDENTIFIED__`. |
| `status` | string | no | Filter logs by status. Example: `blocked`. |
| `search` | string | no | Only return logs matching the search query. Example: `facebook`. |
| `raw` | boolean | no | When true, return all DNS queries instead of the default filtered view. Example: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client": "string",
      "clientIp": "string",
      "device": {},
      "domain": "string",
      "encrypted": true,
      "protocol": "string",
      "reasons": [
        {}
      ],
      "root": "string",
      "status": "string",
      "timestamp": "2026-05-07T12:00:00.000Z",
      "tracker": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client` | string |  |
| `clientIp` | string |  |
| `device` | object |  |
| `domain` | string |  |
| `encrypted` | boolean |  |
| `protocol` | string |  |
| `reasons` | array<object> |  |
| `root` | string |  |
| `status` | string |  |
| `timestamp` | date |  |
| `tracker` | string |  |

## Native endpoint

Through the native NextDNS API, this operation is `GET /profiles/:profile/logs` (base URL `https://api.nextdns.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-logs.md) for the provider-specific parameters and requirements.

