# Ninetailed: List Locales



```
GET https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/list-locales
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninetailed `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/list-locales?connectionId=$CONNECTION_ID&spaceId=string&environmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "spaceId": "string",
  "environmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/list-locales?${params}`, {
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
| `spaceId` | string | yes | Contentful space ID. |
| `environmentId` | string | yes | Contentful environment ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "default": true,
      "fallbackCode": "string",
      "name": "Ava Chen",
      "sys": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `default` | boolean |  |
| `fallbackCode` | string |  |
| `name` | string |  |
| `sys` | object |  |

## Native endpoint

Through the native Ninetailed API, this operation is `GET /spaces/:space_id/environments/:environment_id/locales` (base URL `https://api.contentful.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-locales.md) for the provider-specific parameters and requirements.

