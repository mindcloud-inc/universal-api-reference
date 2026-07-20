# Docupilot: List Content Blocks

Retrieves content blocks from Docupilot.

```
GET https://connect.mindcloud.co/v1/universal/docupilot/latest/actions/list-content-blocks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docupilot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docupilot/latest/actions/list-content-blocks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docupilot/latest/actions/list-content-blocks?${params}`, {
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
| `ordering` | string | no | Which field to use when ordering the results. |
| `page` | number | no | A page number within the paginated result set. |
| `search` | string | no | A search term. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Docupilot API returns.

## Native endpoint

Through the native Docupilot API, this operation is `GET /dashboard/api/v2/content_blocks/` (base URL `https://api.docupilot.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-content-blocks.md) for the provider-specific parameters and requirements.

