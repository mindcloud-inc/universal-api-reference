# Viesus: Get API Version

Retrieves the current Viesus API version.

```
GET https://connect.mindcloud.co/v1/universal/viesus/latest/actions/get-api-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viesus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viesus/latest/actions/get-api-version?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/viesus/latest/actions/get-api-version?${params}`, {
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
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `version` | string | Viesus API version string. |

## Native endpoint

Through the native Viesus API, this operation is `POST /` (base URL `https://api.viesus.cloud/graphql`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-version.md) for the provider-specific parameters and requirements.

