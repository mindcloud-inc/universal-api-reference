# Sales Cookie: Prepare Full Transaction Import

Prepares a transaction import batch in Sales Cookie.

```
POST https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/prepare-full-transaction-import
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sales Cookie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/prepare-full-transaction-import" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dataSource": "string",
  "mappingsXml": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/prepare-full-transaction-import', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dataSource": "string",
    "mappingsXml": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataSource` | string | yes | Data source name sent in the X-DataSource header. |
| `mappingsXml` | string | yes | XML mappings document describing CSV field mappings. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "configuration": {},
      "dataSource": "string",
      "id": "string",
      "query": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `configuration` | object |  |
| `dataSource` | string |  |
| `id` | string |  |
| `query` | string |  |

## Native endpoint

Through the native Sales Cookie API, this operation is `POST /Api/PrepareImport` (base URL `https://salescookie.com/app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/prepare-full-transaction-import.md) for the provider-specific parameters and requirements.

