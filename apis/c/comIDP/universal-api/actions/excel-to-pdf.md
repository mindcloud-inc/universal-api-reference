# ComIDP: Excel to PDF

Creates a ComIDP job to convert an Excel workbook to PDF.

```
POST https://connect.mindcloud.co/v1/universal/comIDP/latest/actions/excel-to-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ComIDP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/comIDP/latest/actions/excel-to-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/comIDP/latest/actions/excel-to-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ComIDP API returns.

## Native endpoint

Through the native ComIDP API, this operation is `POST /server/v2/process/xlsx/pdf` (base URL `https://api-server.compdf.com/server/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/excel-to-pdf.md) for the provider-specific parameters and requirements.

