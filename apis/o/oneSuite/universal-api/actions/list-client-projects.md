# OneSuite: List Client Projects

Retrieves a client's projects from OneSuite.

```
GET https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/list-client-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/list-client-projects?connectionId=$CONNECTION_ID&clientId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/list-client-projects?${params}`, {
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
| `clientId` | string | yes | The ID of the client |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native OneSuite API, this operation is `GET /v1/clients/:client_id/projects` (base URL `https://api.onesuite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-client-projects.md) for the provider-specific parameters and requirements.

