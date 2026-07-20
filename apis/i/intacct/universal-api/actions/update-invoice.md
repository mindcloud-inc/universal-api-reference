# Sage Intacct: Update Invoice



```
PUT https://connect.mindcloud.co/v1/universal/intacct/latest/actions/update-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sage Intacct `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/intacct/latest/actions/update-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "object": "ARINVOICE",
  "fields": "[{\"fieldName\":\"RECORDNO\",\"fieldValue\":\"1102832\"},{\"fieldName\":\"NAME\",\"fieldValue\":\"865215606 - Project Oversight 12\"},{\"fieldName\":\"PROJECTID\",\"fieldValue\":\"42454310\"},{\"fieldName\":\"PBEGINDATE\",\"fieldValue\":\"2023-01-09\"},{\"fieldName\":\"PENDDATE\",\"fieldValue\":\"2023-12-29\"},{\"fieldName\":\"ITEMID\",\"fieldValue\":\"Consulting\"},{\"fieldName\":\"BILLABLE\",\"fieldValue\":true},{\"fieldName\":\"TASKSTATUS\",\"fieldValue\":\"Completed\"}]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intacct/latest/actions/update-invoice', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "object": "ARINVOICE",
    "fields": "[{\"fieldName\":\"RECORDNO\",\"fieldValue\":\"1102832\"},{\"fieldName\":\"NAME\",\"fieldValue\":\"865215606 - Project Oversight 12\"},{\"fieldName\":\"PROJECTID\",\"fieldValue\":\"42454310\"},{\"fieldName\":\"PBEGINDATE\",\"fieldValue\":\"2023-01-09\"},{\"fieldName\":\"PENDDATE\",\"fieldValue\":\"2023-12-29\"},{\"fieldName\":\"ITEMID\",\"fieldValue\":\"Consulting\"},{\"fieldName\":\"BILLABLE\",\"fieldValue\":true},{\"fieldName\":\"TASKSTATUS\",\"fieldValue\":\"Completed\"}]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `object` | string | yes | Default: `ARINVOICE`. |
| `fields` | string | yes | Default: `[{\"fieldName\":\"RECORDNO\",\"fieldValue\":\"1102832\"},{\"fieldName\":\"NAME\",\"fieldValue\":\"865215606 - Project Oversight 12\"},{\"fieldName\":\"PROJECTID\",\"fieldValue\":\"42454310\"},{\"fieldName\":\"PBEGINDATE\",\"fieldValue\":\"2023-01-09\"},{\"fieldName\":\"PENDDATE\",\"fieldValue\":\"2023-12-29\"},{\"fieldName\":\"ITEMID\",\"fieldValue\":\"Consulting\"},{\"fieldName\":\"BILLABLE\",\"fieldValue\":true},{\"fieldName\":\"TASKSTATUS\",\"fieldValue\":\"Completed\"}]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sage Intacct API returns.

## Native endpoint

Through the native Sage Intacct API, this operation is `POST` (base URL `https://api.intacct.com/ia/xml/xmlgw.phtml`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-invoice.md) for the provider-specific parameters and requirements.

