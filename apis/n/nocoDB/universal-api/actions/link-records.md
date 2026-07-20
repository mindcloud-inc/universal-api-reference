# NocoDB: Link Records

Links records through a NocoDB link field.

```
POST https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/link-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NocoDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/link-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "baseId": "string",
  "tableId": "string",
  "linkFieldId": "https://example.com",
  "recordId": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/link-records', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "baseId": "string",
    "tableId": "string",
    "linkFieldId": "https://example.com",
    "recordId": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `baseId` | string | yes | Base identifier. |
| `tableId` | string | yes | Table identifier. |
| `linkFieldId` | string | yes | Link-to-another-record field identifier. |
| `recordId` | string | yes | Record identifier. |
| `id` | string | yes | Adjacent record identifier to link. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native NocoDB API, this operation is `POST /api/v3/data/:baseId/:tableId/links/:linkFieldId/:recordId` (base URL `https://app.nocodb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/link-records.md) for the provider-specific parameters and requirements.

