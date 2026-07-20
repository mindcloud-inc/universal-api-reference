# Mural: Export Mural to File

Creates a new mural export in Mural.

```
POST https://connect.mindcloud.co/v1/universal/mural/latest/actions/export-mural-to-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mural `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mural/latest/actions/export-mural-to-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "muralId": "string",
  "downloadFormat": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mural/latest/actions/export-mural-to-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "muralId": "string",
    "downloadFormat": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `muralId` | string | yes |  |
| `downloadFormat` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "exportId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `exportId` | string |  |

## Native endpoint

Through the native Mural API, this operation is `POST /murals/:muralId/export` (base URL `https://app.mural.co/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-mural-to-file.md) for the provider-specific parameters and requirements.

