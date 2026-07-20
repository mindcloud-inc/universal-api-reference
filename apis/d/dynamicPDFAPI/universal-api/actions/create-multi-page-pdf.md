# DynamicPDF: Create Multi-Page PDF

Creates a multi-page PDF in DynamicPDF API.

```
POST https://connect.mindcloud.co/v1/universal/dynamicPDFAPI/latest/actions/create-multi-page-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DynamicPDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dynamicPDFAPI/latest/actions/create-multi-page-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "instructions": {
    "title": "MindCloud DynamicPDF multi-page test",
    "author": "MindCloud",
    "inputs": [
      {
        "type": "page",
        "elements": [
          {
            "text": "Page 1",
            "type": "text",
            "placement": "topLeft"
          }
        ]
      },
      {
        "type": "page",
        "elements": [
          {
            "text": "Page 2",
            "type": "text",
            "placement": "topLeft"
          }
        ]
      }
    ],
    "creator": "DynamicPDF API"
  }
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dynamicPDFAPI/latest/actions/create-multi-page-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "instructions": {"title":"MindCloud DynamicPDF multi-page test","author":"MindCloud","inputs":[{"type":"page","elements":[{"text":"Page 1","type":"text","placement":"topLeft"}]},{"type":"page","elements":[{"text":"Page 2","type":"text","placement":"topLeft"}]}],"creator":"DynamicPDF API"}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `instructions` | object | yes | DynamicPDF pdf endpoint instructions JSON for a multi-page PDF. Default: `{"title":"MindCloud DynamicPDF multi-page test","author":"MindCloud","inputs":[{"type":"page","elements":[{"text":"Page 1","type":"text","placement":"topLeft"}]},{"type":"page","elements":[{"text":"Page 2","type":"text","placement":"topLeft"}]}],"creator":"DynamicPDF API"}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | number | Generated PDF bytes returned by DynamicPDF. |
| `type` | string | Raw response wrapper type for the generated PDF content. |

## Native endpoint

Through the native DynamicPDF API, this operation is `POST /v1.0/pdf` (base URL `https://api.dpdf.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-multi-page-pdf.md) for the provider-specific parameters and requirements.

