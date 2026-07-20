# Social Intents: List Contacts By Widget

Retrieves contacts from Social Intents by widget ID.

```
GET https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/list-contacts-by-widget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Social Intents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/list-contacts-by-widget?connectionId=$CONNECTION_ID&widgetId=2c9faa989d21dff3019d2b3dd6670023" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "widgetId": "2c9faa989d21dff3019d2b3dd6670023"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/list-contacts-by-widget?${params}`, {
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
| `widgetId` | string | yes | Filter contacts by widget ID. Example: `2c9faa989d21dff3019d2b3dd6670023`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Social Intents API returns.

## Native endpoint

Through the native Social Intents API, this operation is `GET /contacts` (base URL `https://www.socialintents.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts-by-widget.md) for the provider-specific parameters and requirements.

