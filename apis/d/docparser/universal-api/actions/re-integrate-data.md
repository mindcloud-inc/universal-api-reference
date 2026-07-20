# Docparser: Re-Integrate Data

Schedules Docparser documents for re-integration.

```
PUT https://connect.mindcloud.co/v1/universal/docparser/latest/actions/re-integrate-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docparser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/docparser/latest/actions/re-integrate-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "parserId": "string",
  "documentIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docparser/latest/actions/re-integrate-data', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "parserId": "string",
    "documentIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parserId` | string | yes |  |
| `documentIds[]` | array<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "msg": "string",
      "totalReintegrate": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `msg` | string |  |
| `totalReintegrate` | number |  |

## Native endpoint

Through the native Docparser API, this operation is `POST /v1/document/reintegrate/:PARSER_ID` (base URL `https://api.docparser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/re-integrate-data.md) for the provider-specific parameters and requirements.

