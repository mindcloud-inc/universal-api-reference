# FillFaster: Generate PDF

Generates a filled PDF from a FillFaster form.

```
POST https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/generate-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FillFaster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/generate-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/generate-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fid` | string | yes | Form template identifier. |
| `prefillData` | object | no | Field values to render into the generated PDF. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Raw PDF file returned by FillFaster, base64-encoded by the runtime. |

## Native endpoint

Through the native FillFaster API, this operation is `POST /v1/generatePDF` (base URL `https://api.fillfaster.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-pdf.md) for the provider-specific parameters and requirements.

