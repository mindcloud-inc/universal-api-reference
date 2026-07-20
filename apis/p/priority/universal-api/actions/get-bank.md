# Priority: Get Bank

Retrieves a bank from Priority.

```
GET https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-bank
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Priority `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-bank?connectionId=$CONNECTION_ID&bankCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bankCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-bank?${params}`, {
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
| `bankCode` | string | yes | Priority bank code key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "BANKCODE": "string",
      "BANKENAME": "Ava Chen",
      "BANKNAME": "Ava Chen",
      "FIBIFLAG": "string",
      "INACTIVE": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BANKCODE` | string |  |
| `BANKENAME` | string |  |
| `BANKNAME` | string |  |
| `FIBIFLAG` | string |  |
| `INACTIVE` | string |  |

## Native endpoint

Through the native Priority API, this operation is `GET /BANKS(BANKCODE=':bankCode')` (base URL `https://t.eu.priority-connect.online/odata/Priority/tabbtd38.ini/usdemo`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bank.md) for the provider-specific parameters and requirements.

