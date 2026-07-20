# Bitskout: Extract Data from HARO Query

Extracts HARO query data with a Bitskout plugin.

```
POST https://connect.mindcloud.co/v1/universal/bitskout/latest/actions/extract-data-from-haro-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitskout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bitskout/latest/actions/extract-data-from-haro-query" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bitskout/latest/actions/extract-data-from-haro-query', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `text` | string | no | HARO query text to extract structured details from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "outputs": {
        "CATEGORY": "string",
        "DEADLINE": "string",
        "EMAIL": "ava@example.com",
        "MEDIA OUTLET": "string",
        "NAME": "Ava Chen",
        "QUERY": "string",
        "RawJSON": "string",
        "REQUIREMENTS": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `outputs` | object | HARO query extraction outputs |
| `outputs.CATEGORY` | string | Category |
| `outputs.DEADLINE` | string | Deadline |
| `outputs.EMAIL` | string | Email |
| `outputs.MEDIA OUTLET` | string | Media Outlet |
| `outputs.NAME` | string | Name |
| `outputs.QUERY` | string | Query |
| `outputs.RawJSON` | string | Response Raw JSON |
| `outputs.REQUIREMENTS` | string | Requirements |

## Native endpoint

Through the native Bitskout API, this operation is `POST /actions/haro` (base URL `https://api.bitskout.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-data-from-haro-query.md) for the provider-specific parameters and requirements.

