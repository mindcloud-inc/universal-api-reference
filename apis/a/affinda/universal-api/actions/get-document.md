# Affinda: Get specific document

Retrieves a specific document from Affinda.

```
GET https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Affinda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-document?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-document?${params}`, {
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
| `compact` | string | no | If "true", the response is compacted to annotations' parsed data. Annotations' meta data are excluded. Default is "false". |
| `format` | string | no | Specify which format you want the response to be. Default is "json" |
| `identifier` | string | yes | Document's identifier |
| `snakeCase` | string | no | Whether to return the response in snake_case instead of camelCase. Default is false. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "error": {},
      "extractor": "string",
      "meta": {},
      "warnings": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `error` | object |  |
| `extractor` | string |  |
| `meta` | object |  |
| `warnings` | array<object> |  |

## Native endpoint

Through the native Affinda API, this operation is `GET /v3/documents/:identifier` (base URL `https://api.us1.affinda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

