# Transport for London: List Line Routes

Retrieves line routes from Transport for London.

```
GET https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/list-line-routes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transport for London `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/list-line-routes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/list-line-routes?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `serviceTypes` | string | no | Optional comma-separated service types. TfL supports Regular and Night. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "modeName": "Ava Chen",
      "name": "Ava Chen",
      "routeSections": [
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
| `id` | string |  |
| `modeName` | string |  |
| `name` | string |  |
| `routeSections` | array<object> |  |

## Native endpoint

Through the native Transport for London API, this operation is `GET /Line/Route` (base URL `https://api.tfl.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-line-routes.md) for the provider-specific parameters and requirements.

