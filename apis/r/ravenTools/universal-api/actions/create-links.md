# Raven Tools: Create Links

Creates new links in Raven Tools.

```
POST https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/create-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raven Tools `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/create-links" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "link": "JSON array of Raven link objects"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/create-links', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "link": "JSON array of Raven link objects"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain` | string | no | Optional domain if omitted from each link record. Example: `mindcloud.co`. |
| `link` | string | yes | JSON-encoded string representing one or more Raven link records to create. Default: `[{"tags":"bulk,test","domain":"codex-raven-tools-verify-20260408.example","status":"active","link url":"https://mindcloud.co/bulk","link text":"Bulk Raven Link","website url":"https://example.com/bulk","website type":"Other"}]`. Example: `JSON array of Raven link objects`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | number | Created Raven link id. |

## Native endpoint

Through the native Raven Tools API, this operation is `GET /api` (base URL `https://api.raventools.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-links.md) for the provider-specific parameters and requirements.

