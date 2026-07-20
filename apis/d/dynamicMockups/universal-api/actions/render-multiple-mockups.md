# Dynamic Mockups: Render Multiple Mockups

Creates multiple mockup renders in Dynamic Mockups.

```
POST https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/render-multiple-mockups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dynamic Mockups `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/render-multiple-mockups" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "renders": "JSON array of render objects"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/render-multiple-mockups', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "renders": "JSON array of render objects"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `renders` | list<object> | yes | JSON array of render objects. Each item requires mockup_uuid and smart_objects. Example: `JSON array of render objects`. |
| `export_options.image_format` | string | no | Optional export format applied to all renders: jpg, png, or webp. Example: `jpg \| png \| webp`. |
| `export_options.image_size` | number | no | Optional output width in pixels for all renders. Example: `e.g. 1200`. |
| `export_options.mode` | string | no | Optional mode for all renders: view or download. Example: `view \| download`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "failedRenders": 1,
        "renders": [
          {
            "error": "string",
            "mockupUuid": "string",
            "status": "string"
          }
        ],
        "successfulRenders": 1,
        "totalRenders": 1
      },
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.failedRenders` | number |  |
| `data.renders[].error` | string |  |
| `data.renders[].mockupUuid` | string |  |
| `data.renders[].status` | string |  |
| `data.successfulRenders` | number |  |
| `data.totalRenders` | number |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Dynamic Mockups API, this operation is `POST api/v1/renders/batch` (base URL `https://app.dynamicmockups.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/render-multiple-mockups.md) for the provider-specific parameters and requirements.

