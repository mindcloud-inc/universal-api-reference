# Seven: Get Statistics

Retrieves account statistics from Seven.

```
GET https://connect.mindcloud.co/v1/universal/seven/latest/actions/get-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seven/latest/actions/get-statistics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seven/latest/actions/get-statistics?${params}`, {
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
| `start` | date | no | Start date of the statistics in the format YYYY-MM-DD. The date from 30 days ago is set by default. |
| `end` | date | no | End date of the statistics. The current day by default. |
| `label` | string | no | Only shows data for a specific label. |
| `subaccounts` | number | no | Receive data only for the main account, for all your (sub)accounts or only for specific subaccounts ID of a subaccount - Displays the data of a specific subaccount. all - Displays the data of all accounts and subaccounts cumulatively. only_main - Displays only the data of the main account. |
| `groupBy` | date | no | Defines the grouping of the data. The default value is date . |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "hlr": 1,
      "inbound": 1,
      "mnp": 1,
      "rcs": 1,
      "sms": 1,
      "usage_eur": 1,
      "voice": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date |  |
| `hlr` | number |  |
| `inbound` | number |  |
| `mnp` | number |  |
| `rcs` | number |  |
| `sms` | number |  |
| `usage_eur` | number |  |
| `voice` | number |  |

## Native endpoint

Through the native Seven API, this operation is `GET /analytics` (base URL `https://gateway.seven.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-statistics.md) for the provider-specific parameters and requirements.

