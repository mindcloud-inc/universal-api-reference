# Mendeley: Metadata Lookup



```
GET https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/metadata-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendeley `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/metadata-lookup?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/metadata-lookup?${params}`, {
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
| `doi` | string | no | Digital Object Identifier to match. Example: `10.1038/35095137`. |
| `title` | string | no | Title terms to match. Example: `How To Choose a Good Scientific Problem`. |
| `authors` | string | no | Author names to match. Example: `Uri Alon`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Mendeley API returns.

## Native endpoint

Through the native Mendeley API, this operation is `GET /metadata` (base URL `https://api.mendeley.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/metadata-lookup.md) for the provider-specific parameters and requirements.

