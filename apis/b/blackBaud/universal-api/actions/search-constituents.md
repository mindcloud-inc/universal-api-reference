# BlackBaud: Search Constituents



```
GET https://connect.mindcloud.co/v1/universal/blackBaud/latest/actions/search-constituents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlackBaud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blackBaud/latest/actions/search-constituents?connectionId=$CONNECTION_ID&searchText=Name%2C%20email%2C%20or%20lookup%20ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "searchText": "Name, email, or lookup ID"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blackBaud/latest/actions/search-constituents?${params}`, {
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
| `searchText` | string | yes | Text to search across constituent records. Example: `Name, email, or lookup ID`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeInactive` | boolean | no | Include inactive constituents in the search results. Example: `false`. |
| `searchField` | string | no | Optional field to target when running the search. Example: `name`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BlackBaud API returns.

## Native endpoint

Through the native BlackBaud API, this operation is `GET constituent/v1/constituents/search` (base URL `https://api.sky.blackbaud.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-constituents.md) for the provider-specific parameters and requirements.

