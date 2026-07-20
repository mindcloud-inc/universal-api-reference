# ActiveCollab: Get Workspace Info

Retrieves application details from your ActiveCollab workspace.

```
GET https://connect.mindcloud.co/v1/universal/activeCollab/latest/actions/get-workspace-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActiveCollab `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activeCollab/latest/actions/get-workspace-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activeCollab/latest/actions/get-workspace-info?${params}`, {
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
      "application": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `application` | string |  |
| `version` | string |  |

## Native endpoint

Through the native ActiveCollab API, this operation is `GET /info` (base URL `https://app.activecollab.com/:instanceId/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace-info.md) for the provider-specific parameters and requirements.

