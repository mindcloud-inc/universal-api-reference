# Alai: Export Presentation

Creates an async presentation export in Alai.

```
POST https://connect.mindcloud.co/v1/universal/alai/latest/actions/export-presentation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/alai/latest/actions/export-presentation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "presentationId": "string",
  "formats[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/alai/latest/actions/export-presentation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "presentationId": "string",
    "formats[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `presentationId` | string | yes | Target presentation identifier. |
| `formats[]` | array<string> | yes | Requested export formats. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "generationId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `generationId` | string |  |

## Native endpoint

Through the native Alai API, this operation is `POST /presentations/:presentation_id/exports` (base URL `https://slides-api.getalai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-presentation.md) for the provider-specific parameters and requirements.

