# Webling: Get Current Revision



```
GET https://connect.mindcloud.co/v1/universal/webling/latest/actions/get-current-revision
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webling/latest/actions/get-current-revision?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webling/latest/actions/get-current-revision?${params}`, {
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
      "revision": 1,
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `revision` | number |  |
| `version` | number |  |

## Native endpoint

Through the native Webling API, this operation is `GET /replicate` (base URL `https://{{credentials.instanceDomain}}/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-revision.md) for the provider-specific parameters and requirements.

