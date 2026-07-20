# Zeplin: Update Styleguide Text Style

Updates an existing styleguide text style in Zeplin.

```
PUT https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/update-styleguide-text-style
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/update-styleguide-text-style" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "styleguideId": "string",
  "textStyleId": "string",
  "name": "Ava Chen",
  "color": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/update-styleguide-text-style', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "styleguideId": "string",
    "textStyleId": "string",
    "name": "Ava Chen",
    "color": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `styleguideId` | string | yes | Styleguide id |
| `textStyleId` | string | yes | Text style id |
| `name` | string | yes | Name of the text style |
| `color` | object | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zeplin API returns.

## Native endpoint

Through the native Zeplin API, this operation is `PATCH /styleguides/{styleguide_id}/text_styles/{text_style_id}` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-styleguide-text-style.md) for the provider-specific parameters and requirements.

