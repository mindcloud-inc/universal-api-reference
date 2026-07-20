# Bitbucket: Get Repository Settings Inheritance

Retrieves repository settings inheritance from Bitbucket.

```
GET https://connect.mindcloud.co/v1/universal/bitbucket/latest/actions/get-repository-settings-inheritance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitbucket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitbucket/latest/actions/get-repository-settings-inheritance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bitbucket/latest/actions/get-repository-settings-inheritance?${params}`, {
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
| `repo_slug` | string | no | Repository slug. |
| `workspace` | string | no | Workspace slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "inherit_from_project": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `inherit_from_project` | boolean |  |

## Native endpoint

Through the native Bitbucket API, this operation is `GET /repositories/:workspace/:repo_slug/override-settings` (base URL `https://api.bitbucket.org/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-repository-settings-inheritance.md) for the provider-specific parameters and requirements.

