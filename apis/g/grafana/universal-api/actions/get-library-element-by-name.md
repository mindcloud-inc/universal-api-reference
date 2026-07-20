# Grafana: Get Library Element By Name

Retrieves a library element from Grafana by name.

```
GET https://connect.mindcloud.co/v1/universal/grafana/latest/actions/get-library-element-by-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grafana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grafana/latest/actions/get-library-element-by-name?connectionId=$CONNECTION_ID&libraryElementName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "libraryElementName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grafana/latest/actions/get-library-element-by-name?${params}`, {
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
| `libraryElementName` | string | yes | The library element name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "kind": 1,
      "name": "Ava Chen",
      "uid": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `kind` | number |  |
| `name` | string |  |
| `uid` | string |  |
| `version` | number |  |

## Native endpoint

Through the native Grafana API, this operation is `GET /library-elements/name/:library_element_name` (base URL `https://apps78aa.grafana.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-library-element-by-name.md) for the provider-specific parameters and requirements.

