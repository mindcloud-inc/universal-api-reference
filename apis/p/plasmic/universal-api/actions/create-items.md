# Plasmic: Create Items

Creates items in Plasmic CMS.

```
POST https://connect.mindcloud.co/v1/universal/plasmic/latest/actions/create-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Plasmic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/plasmic/latest/actions/create-items" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "modelId": "string",
  "rows[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/plasmic/latest/actions/create-items', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "modelId": "string",
    "rows[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `modelId` | string | yes | The Plasmic CMS model identifier to create rows in. |
| `rows[]` | array<object> | yes | An array of row payloads to create, wrapped as { rows: [...] }. |
| `publish` | string | no | Pass 1 to automatically publish the created rows. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "rows": [
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
| `rows` | array<object> | The created Plasmic CMS rows. |

## Native endpoint

Through the native Plasmic API, this operation is `POST /databases/{{credentials.cmsId}}/tables/:modelId/rows` (base URL `https://data.plasmic.app/api/v1/cms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-items.md) for the provider-specific parameters and requirements.

