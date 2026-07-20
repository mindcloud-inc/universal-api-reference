# AITable.ai: Create Records

Creates new records in a datasheet in AITable.ai.

```
POST https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/create-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AITable.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/create-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "datasheetId": "string",
  "records[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/create-records', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "datasheetId": "string",
    "records[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datasheetId` | string | yes | AITable datasheet ID where records will be created. |
| `records[]` | array<object> | yes | Array of records to create. Each item contains a fields object. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fieldKey` | string | no | Use field names or field IDs when writing fields. AITable supports name or id. Default: `name`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "records": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `records` | array<object> | Created AITable records. |

## Native endpoint

Through the native AITable.ai API, this operation is `POST /fusion/v1/datasheets/:datasheetId/records` (base URL `https://aitable.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-records.md) for the provider-specific parameters and requirements.

