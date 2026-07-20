# ProvenExpert: Create Widget

Creates a widget in ProvenExpert.

```
POST https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/create-widget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProvenExpert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/create-widget" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.type": "portrait",
  "data.width": "180"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/create-widget', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.type": "portrait",
    "data.width": "180"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.type` | string | yes | Type of widget to generate. Example: `portrait`. |
| `data.width` | number | yes | Widget width in pixels. Example: `180`. |
| `data.feedback` | number | no | Whether customer votes should be displayed on the widget. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "html": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `html` | string | Widget embed HTML returned by ProvenExpert. |

## Native endpoint

Through the native ProvenExpert API, this operation is `POST /widget/create` (base URL `https://www.provenexpert.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-widget.md) for the provider-specific parameters and requirements.

