# Supabugs: List Lookup Values

Retrieves issue lookup values from Supabugs.

```
GET https://connect.mindcloud.co/v1/universal/supabugs/latest/actions/list-lookup-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Supabugs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supabugs/latest/actions/list-lookup-values?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supabugs/latest/actions/list-lookup-values?${params}`, {
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
| `type` | string | no | Lookup type: bug_type, bug_severity, bug_priority, or bug_status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "color": "string",
      "id": "string",
      "isFinal": true,
      "isInitial": true,
      "name": "Ava Chen",
      "order": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `color` | string |  |
| `id` | string |  |
| `isFinal` | boolean |  |
| `isInitial` | boolean |  |
| `name` | string |  |
| `order` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Supabugs API, this operation is `GET /lov` (base URL `https://api.supabugs.io/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-lookup-values.md) for the provider-specific parameters and requirements.

