# Sipuni: Export Statistics

Exports filtered call statistics from Sipuni.

```
GET https://connect.mindcloud.co/v1/universal/sipuni/latest/actions/export-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sipuni `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sipuni/latest/actions/export-statistics?connectionId=$CONNECTION_ID&from=DD.MM.YYYY&to=DD.MM.YYYY" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "DD.MM.YYYY",
  "to": "DD.MM.YYYY"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sipuni/latest/actions/export-statistics?${params}`, {
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
| `from` | string | yes | Start date in DD.MM.YYYY format. Example: `DD.MM.YYYY`. |
| `to` | string | yes | End date in DD.MM.YYYY format. Example: `DD.MM.YYYY`. |
| `type` | string | no | 0 all calls, 1 incoming, 2 outgoing, 3 internal. Default: `0`. |
| `state` | string | no | 0 all calls, 1 missed, 2 answered. Default: `0`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `timeFrom` | string | no | Example: `HH:mm`. |
| `timeTo` | string | no | Example: `HH:mm`. |
| `tree` | string | no |  |
| `showTreeId` | string | no | Default: `0`. |
| `fromNumber` | string | no |  |
| `toNumber` | string | no |  |
| `numbersRinged` | string | no | Default: `0`. |
| `numbersInvolved` | string | no | Default: `0`. |
| `names` | string | no | Default: `0`. |
| `outgoingLine` | string | no | Default: `1`. |
| `toAnswer` | string | no |  |
| `anonymous` | string | no | Default: `1`. |
| `firstTime` | string | no | Default: `0`. |
| `dtmfUserAnswer` | string | no | Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Raw CSV response returned by Sipuni. |

## Native endpoint

Through the native Sipuni API, this operation is `GET /statistic/export` (base URL `https://sipuni.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-statistics.md) for the provider-specific parameters and requirements.

