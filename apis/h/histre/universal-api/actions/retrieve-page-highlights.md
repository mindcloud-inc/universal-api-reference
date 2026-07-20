# Histre: Retrieve Page Highlights

Retrieves page highlights from Histre.

```
GET https://connect.mindcloud.co/v1/universal/histre/latest/actions/retrieve-page-highlights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Histre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/histre/latest/actions/retrieve-page-highlights?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/histre/latest/actions/retrieve-page-highlights?${params}`, {
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
| `url` | string | no | Page URL whose highlights should be retrieved. Provide this or Highlight ID. |
| `highlightId` | string | no | Highlight identifier to retrieve. Provide this or URL. |
| `page` | number | no | Optional page number for paginated highlight retrieval. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Histre API returns.

## Native endpoint

Through the native Histre API, this operation is `GET /api/v1/highlight/` (base URL `https://histre.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-page-highlights.md) for the provider-specific parameters and requirements.

