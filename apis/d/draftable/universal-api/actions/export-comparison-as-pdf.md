# Draftable: Export Comparison as PDF

Creates a PDF export job in Draftable.

```
POST https://connect.mindcloud.co/v1/universal/draftable/latest/actions/export-comparison-as-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Draftable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/draftable/latest/actions/export-comparison-as-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "comparison": "string",
  "kind": "combined"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/draftable/latest/actions/export-comparison-as-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "comparison": "string",
    "kind": "combined"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `comparison` | string | yes | The identifier of the comparison to export. |
| `kind` | string | yes | The export format to generate. One of: `combined`, `left`, `right`, `single_page`. |
| `includeCoverPage` | boolean | no | Whether to include a cover page for combined exports. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comparison": "string",
      "errorMessage": "string",
      "failed": true,
      "identifier": "string",
      "includeCoverPage": true,
      "kind": "string",
      "ready": true,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comparison` | string |  |
| `errorMessage` | string |  |
| `failed` | boolean |  |
| `identifier` | string |  |
| `includeCoverPage` | boolean |  |
| `kind` | string |  |
| `ready` | boolean |  |
| `url` | string |  |

## Native endpoint

Through the native Draftable API, this operation is `POST /exports` (base URL `https://api.draftable.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-comparison-as-pdf.md) for the provider-specific parameters and requirements.

