# Transport for London: Get Line Status By Mode

Retrieves line status for modes in Transport for London.

```
GET https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/line-status-by-mode
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transport for London `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/line-status-by-mode?connectionId=$CONNECTION_ID&modes=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "modes": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/line-status-by-mode?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `detail` | boolean | no | Set to true to include details of disruptions causing line status. |

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
      "name": "Ava Chen"
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

## Native endpoint

Through the native Transport for London API, this operation is `GET /Line/Mode/:modes/Status` (base URL `https://api.tfl.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/line-status-by-mode.md) for the provider-specific parameters and requirements.

