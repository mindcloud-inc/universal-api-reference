# Prerender.io: Delete Gsc Integrations

Deletes the GSC integration from Prerender.io.

```
DELETE https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/delete-v3-gsc-integrations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prerender.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/delete-v3-gsc-integrations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/delete-v3-gsc-integrations?${params}`, {
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
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Prerender.io API, this operation is `DELETE /v3/gsc-integrations` (base URL `https://api.prerender.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-v3-gsc-integrations.md) for the provider-specific parameters and requirements.

