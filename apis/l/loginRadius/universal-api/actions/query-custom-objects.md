# LoginRadius: Query Custom Objects

Retrieves custom object records from LoginRadius by query.

```
GET https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/query-custom-objects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoginRadius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/query-custom-objects?connectionId=$CONNECTION_ID&customObject=profileNote" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customObject": "profileNote"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/query-custom-objects?${params}`, {
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
| `customObject` | string | yes | Name of the custom object. Example: `profileNote`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `region` | string | no | Region filter for the results. Example: `us`. |
| `from` | date | no | Start date for the custom object query range. Example: `2026-01-01T00:00:00.000Z`. |
| `to` | date | no | End date for the custom object query range. Example: `2026-12-31T23:59:59.999Z`. |
| `size` | number | no | Maximum number of records to return. Example: `25`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LoginRadius API returns.

## Native endpoint

Through the native LoginRadius API, this operation is `POST https://cloud-api.loginradius.com/customobject` (base URL `https://api.loginradius.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-custom-objects.md) for the provider-specific parameters and requirements.

