# Smartcat: Import Glossary

Creates a glossary import task in Smartcat.

```
POST https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/import-glossary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartcat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/import-glossary" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "glossaryId": "string",
  "clearBeforeImport": true,
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/import-glossary', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "glossaryId": "string",
    "clearBeforeImport": true,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `glossaryId` | string | yes | Glossary ID. |
| `clearBeforeImport` | boolean | yes | Delete existing glossary concepts before import. |
| `file` | file | yes | Glossary import file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "taskId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `taskId` | string | Smartcat glossary import task ID |

## Native endpoint

Through the native Smartcat API, this operation is `POST /api/integration/v1/glossary/import` (base URL `https://smartcat.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-glossary.md) for the provider-specific parameters and requirements.

