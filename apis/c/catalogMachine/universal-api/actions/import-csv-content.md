# Catalog Machine: Import CSV Content

Starts a CSV import job in Catalog Machine.

```
POST https://connect.mindcloud.co/v1/universal/catalogMachine/latest/actions/import-csv-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Catalog Machine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/catalogMachine/latest/actions/import-csv-content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "csv": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/catalogMachine/latest/actions/import-csv-content', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "csv": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `csv` | string | yes | CSV content payload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Errors": [
        {}
      ],
      "JobId": "string",
      "RecordsCount": 1,
      "Success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Errors` | array<object> |  |
| `JobId` | string |  |
| `RecordsCount` | number |  |
| `Success` | boolean |  |

## Native endpoint

Through the native Catalog Machine API, this operation is `POST /import/csv` (base URL `https://www.catalogmachine.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-csv-content.md) for the provider-specific parameters and requirements.

