# DONNAJAMES Easy: Retrain Sources

Retrains URL sources in DONNAJAMES Easy.

```
PUT https://connect.mindcloud.co/v1/universal/dONNAJAMESEasy/latest/actions/retrain-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DONNAJAMES Easy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dONNAJAMESEasy/latest/actions/retrain-sources" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuids[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dONNAJAMESEasy/latest/actions/retrain-sources', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uuids[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uuids[]` | array<string> | yes | URL data source uuids |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "meta_json": "string",
      "modified_at": "string",
      "status": "string",
      "title": "string",
      "tokens": 1,
      "type": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `meta_json` | string |  |
| `modified_at` | string |  |
| `status` | string |  |
| `title` | string |  |
| `tokens` | number |  |
| `type` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native DONNAJAMES Easy API, this operation is `POST data-sources/url/re-scrape` (base URL `https://app.gpt-trainer.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrain-sources.md) for the provider-specific parameters and requirements.

