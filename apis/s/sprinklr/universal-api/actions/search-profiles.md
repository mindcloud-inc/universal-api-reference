# Sprinklr: Search Profiles

Finds profiles in Sprinklr by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/sprinklr/latest/actions/search-profiles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sprinklr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sprinklr/latest/actions/search-profiles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sprinklr/latest/actions/search-profiles?${params}`, {
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
| `snType` | string | no |  |
| `userName` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sprinklr API returns.

## Native endpoint

Through the native Sprinklr API, this operation is `GET api/v2/profile/search` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-profiles.md) for the provider-specific parameters and requirements.

