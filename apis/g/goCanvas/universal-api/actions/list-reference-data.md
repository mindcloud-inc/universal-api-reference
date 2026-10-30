# GoCanvas: List Reference Data



```
GET https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/list-reference-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCanvas `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/list-reference-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/list-reference-data?${params}`, {
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
| `departmentId` | number | no | If omitted, GoCanvas returns reference data from the current user's default department. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "columnCount": 1,
      "departmentId": 1,
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "type": "string",
      "useUserGroups": true,
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `columnCount` | number |  |
| `departmentId` | number |  |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `type` | string |  |
| `useUserGroups` | boolean |  |
| `version` | number |  |

## Native endpoint

Through the native GoCanvas API, this operation is `GET /reference_data` (base URL `https://www.gocanvas.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reference-data.md) for the provider-specific parameters and requirements.

