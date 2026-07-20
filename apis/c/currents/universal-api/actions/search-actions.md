# Currents: Search Actions



```
GET https://connect.mindcloud.co/v1/universal/currents/latest/actions/search-actions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Currents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/currents/latest/actions/search-actions?connectionId=$CONNECTION_ID&projectId=string&search=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "search": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/currents/latest/actions/search-actions?${params}`, {
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
| `projectId` | string | yes |  |
| `search` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `status` | string |  |

## Native endpoint

Through the native Currents API, this operation is `GET /actions` (base URL `https://api.currents.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-actions.md) for the provider-specific parameters and requirements.

