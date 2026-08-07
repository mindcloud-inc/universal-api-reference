# BlackBaud: Search Constituents Duplicate



```
GET https://connect.mindcloud.co/v1/universal/blackBaud/latest/actions/search-constituents-duplicate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlackBaud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blackBaud/latest/actions/search-constituents-duplicate?connectionId=$CONNECTION_ID&lastName=Last%20name" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lastName": "Last name"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blackBaud/latest/actions/search-constituents-duplicate?${params}`, {
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
| `lastName` | string | yes | Last name to use when checking for potential duplicate constituents. Example: `Last name`. |
| `firstName` | string | no | First name to refine duplicate constituent matching. Example: `First name`. |
| `email` | string | no | Email address to refine duplicate constituent matching. Example: `name@example.org`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BlackBaud API returns.

## Native endpoint

Through the native BlackBaud API, this operation is `GET constituent/v1/constituents/duplicatesearch` (base URL `https://api.sky.blackbaud.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-constituents-duplicate.md) for the provider-specific parameters and requirements.

