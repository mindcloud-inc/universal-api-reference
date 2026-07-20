# ArcSite: Export Proposal PDF

Exports a proposal PDF for an ArcSite drawing.

```
POST https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/export-proposal-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ArcSite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/export-proposal-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string",
  "drawingId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/export-proposal-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string",
    "drawingId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | Template ID from proposal templates. |
| `drawingId` | string | yes | Drawing ID to export. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `url` | string |  |

## Native endpoint

Through the native ArcSite API, this operation is `POST /export_proposal_pdf` (base URL `https://api.arcsite.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-proposal-pdf.md) for the provider-specific parameters and requirements.

