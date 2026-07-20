# Weavo Liquid Loom: CSV to Text

Creates text output from CSV in Weavo Liquid Loom.

```
POST https://connect.mindcloud.co/v1/universal/weavoLiquidLoom/latest/actions/csv-to-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weavo Liquid Loom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/weavoLiquidLoom/latest/actions/csv-to-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inputString": "Paste CSV input"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weavoLiquidLoom/latest/actions/csv-to-text', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inputString": "Paste CSV input"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inputString` | string | yes | Input string in CSV format. Example: `Paste CSV input`. |
| `liquidTemplate` | string | no | Optional Liquid template code generated at weavo.dev. For CSV inputs, iterate over the parsed data array for custom mappings. Example: `Paste Liquid template code`. |

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
| `transformedContent` | string | Text content transformed from the CSV input. |

## Native endpoint

Through the native Weavo Liquid Loom API, this operation is `POST /api/CsvToText` (base URL `https://liquidloom.weavo.no`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/csv-to-text.md) for the provider-specific parameters and requirements.

