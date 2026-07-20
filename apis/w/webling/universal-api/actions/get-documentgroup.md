# Webling: Get Documentgroup



```
GET https://connect.mindcloud.co/v1/universal/webling/latest/actions/get-documentgroup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webling/latest/actions/get-documentgroup?connectionId=$CONNECTION_ID&id=259" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "259"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webling/latest/actions/get-documentgroup?${params}`, {
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
| `id` | number | yes | Document group ID to retrieve. Example: `259`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "children": {},
      "links": {},
      "meta": {},
      "parents": [
        1
      ],
      "properties": {},
      "readonly": true,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `children` | object |  |
| `links` | object |  |
| `meta` | object |  |
| `parents` | array<number> |  |
| `properties` | object |  |
| `readonly` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native Webling API, this operation is `GET /documentgroup/:id` (base URL `https://{{credentials.instanceDomain}}/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-documentgroup.md) for the provider-specific parameters and requirements.

