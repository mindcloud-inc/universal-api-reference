# Priority: Get Warehouse

Retrieves a warehouse from Priority.

```
GET https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-warehouse
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Priority `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-warehouse?connectionId=$CONNECTION_ID&warhsName=Ava%20Chen&locName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "warhsName": "Ava Chen",
  "locName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-warehouse?${params}`, {
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
| `warhsName` | string | yes | Priority warehouse name key. |
| `locName` | string | yes | Priority warehouse location key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "COUNTRYNAME": "Ava Chen",
      "LOCNAME": "Ava Chen",
      "TYPE": "string",
      "WARHSDES": "string",
      "WARHSNAME": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `COUNTRYNAME` | string |  |
| `LOCNAME` | string |  |
| `TYPE` | string |  |
| `WARHSDES` | string |  |
| `WARHSNAME` | string |  |

## Native endpoint

Through the native Priority API, this operation is `GET /WAREHOUSES(WARHSNAME=':warhsName',LOCNAME=':locName')` (base URL `https://t.eu.priority-connect.online/odata/Priority/tabbtd38.ini/usdemo`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-warehouse.md) for the provider-specific parameters and requirements.

