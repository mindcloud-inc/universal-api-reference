# Rijksmuseum: List OAI Identifiers



```
GET https://connect.mindcloud.co/v1/universal/rijksmuseum/latest/actions/list-oai-identifiers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rijksmuseum `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rijksmuseum/latest/actions/list-oai-identifiers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rijksmuseum/latest/actions/list-oai-identifiers?${params}`, {
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
| `metadataPrefix` | string | no | OAI-PMH metadata format prefix. Defaults to oai_dc. Default: `oai_dc`. |
| `set` | string | no | Optional OAI-PMH set spec identifier for headers from a curated set. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | no | Optional UTC lower bound timestamp, such as 2026-01-01T00:00:00Z. |
| `until` | string | no | Optional UTC upper bound timestamp, such as 2026-04-01T00:00:00Z. |
| `resumptionToken` | string | no | Token from a previous OAI-PMH ListIdentifiers response for pagination. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Raw OAI-PMH ListIdentifiers XML response. |

## Native endpoint

Through the native Rijksmuseum API, this operation is `GET /oai` (base URL `https://data.rijksmuseum.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-oai-identifiers.md) for the provider-specific parameters and requirements.

