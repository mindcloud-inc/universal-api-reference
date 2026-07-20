# NextDNS: Get Analytics IPs

Retrieves IP query counts from NextDNS analytics.

```
GET https://connect.mindcloud.co/v1/universal/nextDNS/latest/actions/get-analytics-ips
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NextDNS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextDNS/latest/actions/get-analytics-ips?connectionId=$CONNECTION_ID&limit=25&offset=0&profileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "profileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nextDNS/latest/actions/get-analytics-ips?${params}`, {
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
| `profileId` | string | yes | NextDNS profile ID. |
| `from` | date | no | Filter out entities with older date, inclusive. Example: `-7d`. |
| `to` | date | no | Filter out entities with newer or equal date, exclusive. Example: `2026-04-15T00:00:00Z`. |
| `limit` | number | no | Limit the number of results returned. Example: `10`. |
| `cursor` | string | no | Use the pagination cursor returned by the previous response. Example: `j2k3zl3b4v`. |
| `device` | string | no | Only get entities related to a specific device. Example: `__UNIDENTIFIED__`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "geo": {},
      "ip": "string",
      "network": {},
      "queries": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `geo` | object |  |
| `ip` | string |  |
| `network` | object |  |
| `queries` | number |  |

## Native endpoint

Through the native NextDNS API, this operation is `GET /profiles/:profile/analytics/ips` (base URL `https://api.nextdns.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-analytics-ips.md) for the provider-specific parameters and requirements.

