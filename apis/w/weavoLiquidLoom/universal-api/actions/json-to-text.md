# Weavo Liquid Loom: JSON to Text

Creates text output from JSON in Weavo Liquid Loom.

```
POST https://connect.mindcloud.co/v1/universal/weavoLiquidLoom/latest/actions/json-to-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weavo Liquid Loom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/weavoLiquidLoom/latest/actions/json-to-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inputString": "Paste JSON input"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weavoLiquidLoom/latest/actions/json-to-text', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inputString": "Paste JSON input"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inputString` | string | yes | Input string in JSON format. Example: `Paste JSON input`. |
| `liquidTemplate` | string | no | Optional Liquid template code generated at weavo.dev for custom mappings. Example: `Paste Liquid template code`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `logFileName` | string | no | Name of the log file. Only applicable when logging is enabled. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "transformedContent": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `transformedContent` | string | Text content transformed from the JSON input. |

## Native endpoint

Through the native Weavo Liquid Loom API, this operation is `POST /api/JsonToText` (base URL `https://liquidloom.weavo.no`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/json-to-text.md) for the provider-specific parameters and requirements.

