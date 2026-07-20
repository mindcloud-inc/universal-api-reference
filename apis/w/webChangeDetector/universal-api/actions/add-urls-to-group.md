# WebChange Detector: Add URLs To Group

Adds URLs to a group in WebChange Detector.

```
PUT https://connect.mindcloud.co/v1/universal/webChangeDetector/latest/actions/add-urls-to-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebChange Detector `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/webChangeDetector/latest/actions/add-urls-to-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "urls[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webChangeDetector/latest/actions/add-urls-to-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "urls[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `urls[]` | array<object> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |

## Native endpoint

Through the native WebChange Detector API, this operation is `POST /api/v2/groups/:id/add-urls` (base URL `https://api.webchangedetector.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-urls-to-group.md) for the provider-specific parameters and requirements.

