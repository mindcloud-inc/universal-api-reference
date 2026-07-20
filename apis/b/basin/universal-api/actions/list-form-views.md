# Basin: List Form Views

Retrieves form view records from Basin.

```
GET https://connect.mindcloud.co/v1/universal/basin/latest/actions/list-form-views
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Basin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/basin/latest/actions/list-form-views?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/basin/latest/actions/list-form-views?${params}`, {
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
| `query` | string | no | Filter form views by ID, UUID, form ID, or form UUID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Basin API returns.

## Native endpoint

Through the native Basin API, this operation is `GET /api/v1/form_views` (base URL `https://usebasin.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-views.md) for the provider-specific parameters and requirements.

