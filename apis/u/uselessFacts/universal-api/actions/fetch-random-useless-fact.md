# Useless Facts: Fetch Random Useless Fact



```
GET https://connect.mindcloud.co/v1/universal/uselessFacts/latest/actions/fetch-random-useless-fact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Useless Facts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uselessFacts/latest/actions/fetch-random-useless-fact?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uselessFacts/latest/actions/fetch-random-useless-fact?${params}`, {
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
| `language` | list<string> | no | Optional fact language. The provider documents English (en) and German (de). One of: `de`, `en`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "language": "string",
      "permalink": "https://example.com",
      "source": "string",
      "source_url": "https://example.com",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Provider fact identifier. |
| `language` | string | Language code of the returned fact. |
| `permalink` | string | Provider permalink for the returned fact. |
| `source` | string | Provider-supplied fact source. |
| `source_url` | string | Provider-supplied source URL. |
| `text` | string | Useless fact text. |

## Native endpoint

Through the native Useless Facts API, this operation is `GET /api/v2/facts/random` (base URL `https://uselessfacts.jsph.pl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-random-useless-fact.md) for the provider-specific parameters and requirements.

