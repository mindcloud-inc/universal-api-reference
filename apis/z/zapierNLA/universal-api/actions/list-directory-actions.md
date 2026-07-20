# Zapier NLA: List Directory Actions



```
GET https://connect.mindcloud.co/v1/universal/zapierNLA/latest/actions/list-directory-actions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zapier NLA `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zapierNLA/latest/actions/list-directory-actions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zapierNLA/latest/actions/list-directory-actions?${params}`, {
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
| `query` | string | no | Search term for directory actions. |
| `includeExposed` | boolean | no | Include actions currently exposed by the Zapier account. Default: `false`. |
| `count` | number | no | Maximum number of directory actions to return. Default: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "app": {},
      "configuration_link": "https://example.com",
      "key": "string",
      "name": "Ava Chen",
      "results": [
        {}
      ],
      "score": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `app` | object |  |
| `configuration_link` | string |  |
| `key` | string |  |
| `name` | string |  |
| `results` | array<object> |  |
| `score` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Zapier NLA API, this operation is `GET /api/v1/search/actions/` (base URL `https://actions.zapier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-directory-actions.md) for the provider-specific parameters and requirements.

