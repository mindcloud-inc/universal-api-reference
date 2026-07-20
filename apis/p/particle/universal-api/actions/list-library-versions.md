# Particle: List Library Versions



```
GET https://connect.mindcloud.co/v1/universal/particle/latest/actions/list-library-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Particle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/particle/latest/actions/list-library-versions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/particle/latest/actions/list-library-versions?${params}`, {
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
      "data": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |

## Native endpoint

Through the native Particle API, this operation is `GET /v1/libraries/:libraryName/versions` (base URL `https://api.particle.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-library-versions.md) for the provider-specific parameters and requirements.

