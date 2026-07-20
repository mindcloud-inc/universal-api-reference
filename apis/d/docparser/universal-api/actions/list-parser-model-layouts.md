# Docparser: List Parser Model Layouts

Retrieves parser model layouts from Docparser.

```
GET https://connect.mindcloud.co/v1/universal/docparser/latest/actions/list-parser-model-layouts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docparser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docparser/latest/actions/list-parser-model-layouts?connectionId=$CONNECTION_ID&parserId=tiumtyrcddpn" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "parserId": "tiumtyrcddpn"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docparser/latest/actions/list-parser-model-layouts?${params}`, {
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
| `parserId` | string | yes | Use the parser ID returned by List Document Parsers. Example: `tiumtyrcddpn`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Docparser API returns.

## Native endpoint

Through the native Docparser API, this operation is `GET /v1/parser/models/:PARSER_ID` (base URL `https://api.docparser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-parser-model-layouts.md) for the provider-specific parameters and requirements.

