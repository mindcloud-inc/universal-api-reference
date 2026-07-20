# FEMA: List IPAWS Archived Alerts

Retrieves IPAWS archived alerts from FEMA.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-ipaws-archived-alerts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-ipaws-archived-alerts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-ipaws-archived-alerts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": "string",
      "code": [
        "string"
      ],
      "cogId": 1,
      "id": "string",
      "identifier": "string",
      "info": [
        {}
      ],
      "msgType": "string",
      "note": "string",
      "originalMessage": "string",
      "restriction": "string",
      "scope": "string",
      "sender": "ava@example.com",
      "sent": "2026-05-07T12:00:00.000Z",
      "source": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | string |  |
| `code` | array<string> |  |
| `cogId` | number |  |
| `id` | string |  |
| `identifier` | string |  |
| `info` | array<object> |  |
| `msgType` | string |  |
| `note` | string |  |
| `originalMessage` | string |  |
| `restriction` | string |  |
| `scope` | string |  |
| `sender` | string |  |
| `sent` | date |  |
| `source` | string |  |
| `status` | string |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v1/IpawsArchivedAlerts` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-ipaws-archived-alerts.md) for the provider-specific parameters and requirements.

