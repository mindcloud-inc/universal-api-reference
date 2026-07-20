# BSC Designer: Get All Indicator Values For Document



```
GET https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/get-all-indicator-values-for-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BSC Designer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/get-all-indicator-values-for-document?connectionId=$CONNECTION_ID&docId=string&date=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "docId": "string",
  "date": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/get-all-indicator-values-for-document?${params}`, {
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
| `docId` | string | yes | Document ID or alias. |
| `date` | string | yes | Date in yyyy-MM-dd format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "values": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `values` | array<object> | All indicator values for the document at the requested date. |

## Native endpoint

Through the native BSC Designer API, this operation is `GET /rest/api/document/:docId/kpi/batch/all/get-value/:date` (base URL `https://www.webbsc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-indicator-values-for-document.md) for the provider-specific parameters and requirements.

