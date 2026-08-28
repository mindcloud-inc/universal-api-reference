# MindCloud: List Universal Apps



```
GET https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/list-universal-apps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MindCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/list-universal-apps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/list-universal-apps?${params}`, {
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
| `actionQ` | string | no | Optional Action Query query parameter documented by the MindCloud v2 API. |
| `fields` | string | no | Optional Fields query parameter documented by the MindCloud v2 API. |
| `limit` | number | no | Optional Limit query parameter documented by the MindCloud v2 API. |
| `offset` | number | no | Optional Offset query parameter documented by the MindCloud v2 API. |
| `q` | string | no | Optional Search Query query parameter documented by the MindCloud v2 API. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Returned records. |
| `success` | boolean | Whether the request succeeded. |

## Native endpoint

Through the native MindCloud API, this operation is `GET /v2/universal/apps` (base URL `https://connect.mindcloud.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-universal-apps.md) for the provider-specific parameters and requirements.

