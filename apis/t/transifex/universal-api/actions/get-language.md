# Transifex: Get Language



```
GET https://connect.mindcloud.co/v1/universal/transifex/latest/actions/get-language
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transifex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transifex/latest/actions/get-language?connectionId=$CONNECTION_ID&languageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "languageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transifex/latest/actions/get-language?${params}`, {
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
| `languageId` | string | yes | The Transifex language identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "code": "string",
        "name": "Ava Chen",
        "plural_equation": "string",
        "plural_rules": {
          "one": "string",
          "other": "string"
        },
        "rtl": true
      },
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.code` | string |  |
| `attributes.name` | string |  |
| `attributes.plural_equation` | string |  |
| `attributes.plural_rules.one` | string |  |
| `attributes.plural_rules.other` | string |  |
| `attributes.rtl` | boolean |  |
| `id` | string |  |
| `links.self` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Transifex API, this operation is `GET /languages/:language_id` (base URL `https://rest.api.transifex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-language.md) for the provider-specific parameters and requirements.

