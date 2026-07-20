# Rollbar: Delete Project Access Token By Path

Deletes a project access token from Rollbar by path identifier.

```
DELETE https://connect.mindcloud.co/v1/universal/rollbar/latest/actions/delete-project-access-token-by-path
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rollbar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/rollbar/latest/actions/delete-project-access-token-by-path?connectionId=$CONNECTION_ID&projectId=1&tokenIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1",
  "tokenIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rollbar/latest/actions/delete-project-access-token-by-path?${params}`, {
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
| `projectId` | number | yes | Rollbar project identifier |
| `tokenIdentifier` | string | yes | Project access token identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "err": 1,
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `err` | number |  |
| `result` | object |  |

## Native endpoint

Through the native Rollbar API, this operation is `DELETE /project/:projectId/access_token/:tokenIdentifier` (base URL `https://api.rollbar.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-project-access-token-by-path.md) for the provider-specific parameters and requirements.

