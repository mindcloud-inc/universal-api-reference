# Bitbucket: Get Repository Branching Model Settings

Retrieves repository branching model settings from Bitbucket.

```
GET https://connect.mindcloud.co/v1/universal/bitbucket/latest/actions/get-repository-branching-model-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitbucket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitbucket/latest/actions/get-repository-branching-model-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bitbucket/latest/actions/get-repository-branching-model-settings?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "branch_types": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `branch_types` | object |  |

## Native endpoint

Through the native Bitbucket API, this operation is `GET /repositories/:workspace/:repo_slug/branching-model/settings` (base URL `https://api.bitbucket.org/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-repository-branching-model-settings.md) for the provider-specific parameters and requirements.

