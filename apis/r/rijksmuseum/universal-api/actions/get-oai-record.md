# Rijksmuseum: Get OAI Record



```
GET https://connect.mindcloud.co/v1/universal/rijksmuseum/latest/actions/get-oai-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rijksmuseum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rijksmuseum/latest/actions/get-oai-record?connectionId=$CONNECTION_ID&identifier=https%3A%2F%2Fid.rijksmuseum.nl%2F200107928" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "https://id.rijksmuseum.nl/200107928"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rijksmuseum/latest/actions/get-oai-record?${params}`, {
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
| `identifier` | string | yes | Full OAI-PMH object identifier URI, such as https://id.rijksmuseum.nl/200107928. Default: `https://id.rijksmuseum.nl/200107928`. |

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
| `response` | string | Raw OAI-PMH GetRecord XML response. |

## Native endpoint

Through the native Rijksmuseum API, this operation is `GET /oai` (base URL `https://data.rijksmuseum.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-oai-record.md) for the provider-specific parameters and requirements.

