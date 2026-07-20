# Smartcat: Request Glossary Export

Creates a glossary export task in Smartcat.

```
POST https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/request-glossary-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartcat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/request-glossary-export" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "glossaryId": "glossary-id"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/request-glossary-export', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "glossaryId": "glossary-id"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `glossaryId` | string | yes | Smartcat glossary ID to export. Example: `glossary-id`. |

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
| `taskId` | string | Smartcat glossary export task ID |

## Native endpoint

Through the native Smartcat API, this operation is `POST /api/integration/v1/glossary/export` (base URL `https://smartcat.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-glossary-export.md) for the provider-specific parameters and requirements.

