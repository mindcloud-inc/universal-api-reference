# DocuWriter.ai: Generate UML Diagram



```
POST https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/generate-uml-diagram
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuWriter.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/generate-uml-diagram" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceCode": "string",
  "filename": "Ava Chen",
  "diagramType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/generate-uml-diagram', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceCode": "string",
    "filename": "Ava Chen",
    "diagramType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceCode` | string | yes | Raw source code to analyze. |
| `filename` | string | yes | Name of the source file. |
| `diagramType` | string | yes | Type of UML diagram to generate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "diagramType": "string",
      "generation": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `diagramType` | string | Diagram type returned by the provider. |
| `generation` | string | Generated UML diagram content. |

## Native endpoint

Through the native DocuWriter.ai API, this operation is `POST /api/generate-uml-diagram` (base URL `https://app.docuwriter.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-uml-diagram.md) for the provider-specific parameters and requirements.

