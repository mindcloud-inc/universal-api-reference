# Transport for London: Get Lines By Mode

Retrieves lines for selected modes in Transport for London.

```
GET https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/lines-by-mode
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transport for London `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/lines-by-mode?connectionId=$CONNECTION_ID&modes=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "modes": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/lines-by-mode?${params}`, {
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
| `modes` | string | yes | Comma-separated mode names, such as tube,dlr,bus. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "lineStatuses": [
        {}
      ],
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
| `lineStatuses` | array<object> |  |
| `modeName` | string |  |
| `name` | string |  |
| `routeSections` | array<object> |  |

## Native endpoint

Through the native Transport for London API, this operation is `GET /Line/Mode/:modes` (base URL `https://api.tfl.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lines-by-mode.md) for the provider-specific parameters and requirements.

