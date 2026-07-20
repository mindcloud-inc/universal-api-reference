# Make: List Scenarios

Lists scenarios for the specified team.

```
GET https://connect.mindcloud.co/v1/universal/make/latest/actions/list-scenarios
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Make `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/make/latest/actions/list-scenarios?connectionId=$CONNECTION_ID&teamId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/make/latest/actions/list-scenarios?${params}`, {
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
| `teamId` | number | yes | The ID of the Make team whose scenarios should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "isActive": true,
      "name": "Ava Chen",
      "organizationId": 1,
      "teamId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `isActive` | boolean |  |
| `name` | string |  |
| `organizationId` | number |  |
| `teamId` | number |  |

## Native endpoint

Through the native Make API, this operation is `GET /scenarios` (base URL `https://us2.make.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-scenarios.md) for the provider-specific parameters and requirements.

