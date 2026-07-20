# Kameleoon: Get all tags



```
GET https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kameleoon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-tags?connectionId=$CONNECTION_ID&paramsIo=page%3D1%2C%20perPage%3D20&type=EXPERIMENT" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "paramsIo": "page=1, perPage=20",
  "type": "EXPERIMENT"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-tags?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `paramsIo` | string | yes | Required query object documented by Kameleoon for list endpoints. Example: `page=1, perPage=20`. |
| `type` | string | yes | Tag type filter required by Kameleoon tags endpoint. Valid values include EXPERIMENT, FEATURE, PERSONALIZATION, SEGMENT, GOAL, WIDGET, STUDIO_THEME, TEAM, IMAGE, AI_EXPLORATION_SCOPE, KEY_MOMENT. Default: `EXPERIMENT`. Example: `EXPERIMENT`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Kameleoon API, this operation is `GET tags` (base URL `https://api.kameleoon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-tags.md) for the provider-specific parameters and requirements.

