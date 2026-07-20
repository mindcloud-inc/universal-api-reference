# Priority: Get Quotation Document

Retrieves a quotation document from Priority.

```
GET https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-quotation-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Priority `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-quotation-document?connectionId=$CONNECTION_ID&docNo=string&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "docNo": "string",
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-quotation-document?${params}`, {
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
| `docNo` | string | yes | Priority document number key. |
| `type` | string | yes | Priority document type key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ACTIVEFLAG": "string",
      "CUSTNAME": "Ava Chen",
      "DOCNO": "string",
      "STARTDATE": "2026-05-07T12:00:00.000Z",
      "TYPE": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ACTIVEFLAG` | string |  |
| `CUSTNAME` | string |  |
| `DOCNO` | string |  |
| `STARTDATE` | date |  |
| `TYPE` | string |  |

## Native endpoint

Through the native Priority API, this operation is `GET /DOCUMENTS_Q(DOCNO=':docNo',TYPE=':type')` (base URL `https://t.eu.priority-connect.online/odata/Priority/tabbtd38.ini/usdemo`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-quotation-document.md) for the provider-specific parameters and requirements.

