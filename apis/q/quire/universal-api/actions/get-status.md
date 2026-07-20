# Quire: Get Status

Retrieves a status from a Quire project.

```
GET https://connect.mindcloud.co/v1/universal/quire/latest/actions/get-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quire/latest/actions/get-status?connectionId=$CONNECTION_ID&projectId=string&value=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "value": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quire/latest/actions/get-status?${params}`, {
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
| `projectId` | string | yes | Project ID. |
| `value` | number | yes | Status value to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "name": "Ava Chen",
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `name` | string |  |
| `value` | number |  |

## Native endpoint

Through the native Quire API, this operation is `GET status/id/:projectId/:value` (base URL `https://quire.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-status.md) for the provider-specific parameters and requirements.

