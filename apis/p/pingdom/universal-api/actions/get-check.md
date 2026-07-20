# Pingdom: Get Check



```
GET https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/get-check
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pingdom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/get-check?connectionId=$CONNECTION_ID&checkId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "checkId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/get-check?${params}`, {
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
| `checkId` | number | yes | Identifier of the check to retrieve. |
| `includeTeams` | boolean | no | Include team connections for the check. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "customMessage": "string",
      "hostname": "Ava Chen",
      "id": 1,
      "integrationids": [
        1
      ],
      "ipv6": true,
      "name": "Ava Chen",
      "notifyagainevery": 1,
      "notifywhenbackup": true,
      "probeFilters": [
        "string"
      ],
      "resolution": 1,
      "responsetimeThreshold": 1,
      "sendnotificationwhendown": 1,
      "status": "string",
      "tags": [
        {}
      ],
      "type": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number | UNIX time when the check was created. |
| `customMessage` | string | Custom alert message. |
| `hostname` | string | Target hostname. |
| `id` | number | Check identifier. |
| `integrationids` | array<number> | Integration identifiers linked to the check. |
| `ipv6` | boolean | Whether the check uses IPv6. |
| `name` | string | Check name. |
| `notifyagainevery` | number | How often to repeat notifications after the initial alert. |
| `notifywhenbackup` | boolean | Whether to notify when the check comes back up. |
| `probeFilters` | array<string> | Probe filter values configured on the check. |
| `resolution` | number | Check interval in minutes. |
| `responsetimeThreshold` | number | Configured response-time threshold in milliseconds. |
| `sendnotificationwhendown` | number | How many down results trigger a notification. |
| `status` | string | Current check status. |
| `tags` | array<object> | Tags assigned to the check. |
| `type` | object | Type-specific check configuration. |

## Native endpoint

Through the native Pingdom API, this operation is `GET /checks/:checkid` (base URL `https://api.pingdom.com/api/3.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-check.md) for the provider-specific parameters and requirements.

