# Pushover: Update Glance



```
PUT https://connect.mindcloud.co/v1/universal/pushover/latest/actions/update-glance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushover `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pushover/latest/actions/update-glance" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "user": "Pushover user key"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushover/latest/actions/update-glance', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "user": "Pushover user key"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `user` | string | yes | Pushover user key for the widget owner. Example: `Pushover user key`. |
| `title` | string | no | Short description shown for the glance data. Example: `Widgets Sold`. |
| `text` | string | no | Main glance text shown on most screens. Example: `30`. |
| `subtext` | string | no | Secondary line of glance data. Example: `Today`. |
| `count` | number | no | Integer count shown on smaller screens. Example: `30`. |
| `percent` | number | no | Progress percentage from 0 through 100. Example: `75`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `device` | string | no | Optional device name to target a specific widget. Example: `iphone`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "request": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `request` | string | Pushover request identifier. |
| `status` | number | API status. Returns 1 when the glance update succeeds. |

## Native endpoint

Through the native Pushover API, this operation is `POST /glances.json` (base URL `https://api.pushover.net/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-glance.md) for the provider-specific parameters and requirements.

