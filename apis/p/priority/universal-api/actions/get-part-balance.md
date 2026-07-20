# Priority: Get Part Balance

Retrieves a part balance from Priority.

```
GET https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-part-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Priority `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-part-balance?connectionId=$CONNECTION_ID&warhs=1&part=1&cust=1&act=1&serial=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "warhs": "1",
  "part": "1",
  "cust": "1",
  "act": "1",
  "serial": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-part-balance?${params}`, {
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
| `warhs` | number | yes | Priority warehouse key for the part balance lookup. |
| `part` | number | yes | Priority part key for the part balance lookup. |
| `cust` | number | yes | Priority customer segment of the composite part balance key. |
| `act` | number | yes | Priority activity segment of the composite part balance key. |
| `serial` | number | yes | Priority serial segment of the composite part balance key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "BALANCE": 1,
      "CUSTNAME": "Ava Chen",
      "LOCNAME": "Ava Chen",
      "PARTNAME": "Ava Chen",
      "WARHSNAME": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BALANCE` | number |  |
| `CUSTNAME` | string |  |
| `LOCNAME` | string |  |
| `PARTNAME` | string |  |
| `WARHSNAME` | string |  |

## Native endpoint

Through the native Priority API, this operation is `GET /PARTBAL(WARHS=:warhs,PART=:part,CUST=:cust,ACT=:act,SERIAL=:serial)` (base URL `https://t.eu.priority-connect.online/odata/Priority/tabbtd38.ini/usdemo`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-part-balance.md) for the provider-specific parameters and requirements.

