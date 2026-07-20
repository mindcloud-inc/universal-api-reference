# Make: List Teams

Lists the teams in the specified organization.

```
GET https://connect.mindcloud.co/v1/universal/make/latest/actions/list-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Make `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/make/latest/actions/list-teams?connectionId=$CONNECTION_ID&organizationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/make/latest/actions/list-teams?${params}`, {
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
| `organizationId` | number | yes | The ID of the Make organization whose teams should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "globalAgentsEnabled": true,
      "id": 1,
      "name": "Ava Chen",
      "organizationId": 1,
      "scenarioDrafts": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `globalAgentsEnabled` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `organizationId` | number |  |
| `scenarioDrafts` | boolean |  |

## Native endpoint

Through the native Make API, this operation is `GET /teams` (base URL `https://us2.make.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-teams.md) for the provider-specific parameters and requirements.

