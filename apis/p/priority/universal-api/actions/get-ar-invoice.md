# Priority: Get AR Invoice

Retrieves an AR invoice from Priority.

```
GET https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-ar-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Priority `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-ar-invoice?connectionId=$CONNECTION_ID&ivNum=string&debit=string&ivType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ivNum": "string",
  "debit": "string",
  "ivType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-ar-invoice?${params}`, {
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
| `ivNum` | string | yes | Priority invoice number key. |
| `debit` | string | yes | Priority debit indicator key. |
| `ivType` | string | yes | Priority invoice type key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CUSTNAME": "Ava Chen",
      "DEBIT": "string",
      "IVDATE": "2026-05-07T12:00:00.000Z",
      "IVNUM": "string",
      "IVTYPE": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CUSTNAME` | string |  |
| `DEBIT` | string |  |
| `IVDATE` | date |  |
| `IVNUM` | string |  |
| `IVTYPE` | string |  |

## Native endpoint

Through the native Priority API, this operation is `GET /AINVOICES(IVNUM=':ivNum',DEBIT=':debit',IVTYPE=':ivType')` (base URL `https://t.eu.priority-connect.online/odata/Priority/tabbtd38.ini/usdemo`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ar-invoice.md) for the provider-specific parameters and requirements.

