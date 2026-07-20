# Pingdom: List Check Results



```
GET https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/list-check-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pingdom `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/list-check-results?connectionId=$CONNECTION_ID&limit=25&offset=0&checkId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "checkId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/list-check-results?${params}`, {
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
| `checkId` | number | yes | Identifier of the check. |
| `from` | number | no | Start of the results time range as UNIX time. |
| `to` | number | no | End of the results time range as UNIX time. |
| `probes` | string | no | Comma-separated list of probe identifiers. |
| `status` | string | no | Comma-separated list of result statuses. |
| `includeAnalysis` | boolean | no | Include available root-cause analysis identifiers. |
| `maxResponse` | number | no | Maximum response time in milliseconds. |
| `minResponse` | number | no | Minimum response time in milliseconds. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "probeid": 1,
      "responsetime": 1,
      "status": "string",
      "statusdesc": "string",
      "statusdesclong": "string",
      "time": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `probeid` | number |  |
| `responsetime` | number |  |
| `status` | string |  |
| `statusdesc` | string |  |
| `statusdesclong` | string |  |
| `time` | number |  |

## Native endpoint

Through the native Pingdom API, this operation is `GET /results/:checkid` (base URL `https://api.pingdom.com/api/3.1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-check-results.md) for the provider-specific parameters and requirements.

