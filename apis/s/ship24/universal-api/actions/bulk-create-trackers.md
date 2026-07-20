# Ship24: Bulk Create Trackers

Creates multiple new trackers in Ship24.

```
POST https://connect.mindcloud.co/v1/universal/ship24/latest/actions/bulk-create-trackers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ship24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ship24/latest/actions/bulk-create-trackers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "trackers[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ship24/latest/actions/bulk-create-trackers', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "trackers[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `trackers[]` | array<object> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        {}
      ],
      "inputData": {},
      "itemStatus": "string",
      "tracker": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<object> | Per-item error details when creation fails. |
| `inputData` | object | Payload used to create the tracker. |
| `itemStatus` | string | Status of the individual tracker creation result. |
| `tracker` | object | Tracker object returned for created or existing items. |

## Native endpoint

Through the native Ship24 API, this operation is `POST /public/v1/trackers/bulk` (base URL `https://api.ship24.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-create-trackers.md) for the provider-specific parameters and requirements.

