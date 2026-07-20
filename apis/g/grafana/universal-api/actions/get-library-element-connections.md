# Grafana: Get Library Element Connections

Retrieves library element connections from Grafana.

```
GET https://connect.mindcloud.co/v1/universal/grafana/latest/actions/get-library-element-connections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grafana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grafana/latest/actions/get-library-element-connections?connectionId=$CONNECTION_ID&libraryElementUid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "libraryElementUid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grafana/latest/actions/get-library-element-connections?${params}`, {
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
| `libraryElementUid` | string | yes | The library element UID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "connectionUid": "string",
      "id": 1,
      "kind": 1,
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connectionUid` | string |  |
| `id` | number |  |
| `kind` | number |  |
| `uid` | string |  |

## Native endpoint

Through the native Grafana API, this operation is `GET /library-elements/:library_element_uid/connections/` (base URL `https://apps78aa.grafana.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-library-element-connections.md) for the provider-specific parameters and requirements.

