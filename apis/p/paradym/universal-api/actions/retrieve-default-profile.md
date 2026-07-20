# Paradym: Retrieve Default Profile

Retrieves the default project profile from Paradym.

```
GET https://connect.mindcloud.co/v1/universal/paradym/latest/actions/retrieve-default-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paradym `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paradym/latest/actions/retrieve-default-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paradym/latest/actions/retrieve-default-profile?${params}`, {
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
      "displayName": "Ava Chen",
      "id": "string",
      "openId4VcVersion": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string |  |
| `id` | string |  |
| `openId4VcVersion` | string |  |

## Native endpoint

Through the native Paradym API, this operation is `GET /projects/:projectId/profiles/default` (base URL `https://api.paradym.id/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-default-profile.md) for the provider-specific parameters and requirements.

