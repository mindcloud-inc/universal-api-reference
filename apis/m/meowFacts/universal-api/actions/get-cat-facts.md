# Meow Facts: Get cat facts



```
GET https://connect.mindcloud.co/v1/universal/meowFacts/latest/actions/get-cat-facts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meow Facts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/meowFacts/latest/actions/get-cat-facts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/meowFacts/latest/actions/get-cat-facts?${params}`, {
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
| `count` | number | no | Optional number of cat facts to return. |
| `id` | number | no | Optional fact ID or order to retrieve. |
| `lang` | string | no | Optional documented language code for localized cat facts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<string> | Localized cat facts returned by the provider. |

## Native endpoint

Through the native Meow Facts API, this operation is `GET /` (base URL `https://meowfacts.herokuapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cat-facts.md) for the provider-specific parameters and requirements.

