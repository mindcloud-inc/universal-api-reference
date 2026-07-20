# MoySklad: List custom templates

Retrieves custom templates from MoySklad.

```
GET https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/list-custom-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoySklad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/list-custom-templates?connectionId=$CONNECTION_ID&entityType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entityType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/list-custom-templates?${params}`, {
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
| `entityType` | string | yes | MoySklad document type that supports custom templates. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "context": {},
      "meta": {},
      "rows": [
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
| `context` | object |  |
| `meta` | object |  |
| `rows` | array<object> |  |

## Native endpoint

Through the native MoySklad API, this operation is `GET entity/:entityType/metadata/customtemplate` (base URL `https://api.moysklad.ru/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-templates.md) for the provider-specific parameters and requirements.

