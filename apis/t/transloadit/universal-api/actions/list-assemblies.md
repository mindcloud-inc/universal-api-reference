# Transloadit: List Assemblies

Retrieves a list of assemblies from Transloadit.

```
GET https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/list-assemblies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transloadit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/list-assemblies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/list-assemblies?${params}`, {
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
      "count": 1,
      "items": [
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
| `count` | number | Number of assemblies returned. |
| `items` | array<object> | Assemblies returned by Transloadit. |

## Native endpoint

Through the native Transloadit API, this operation is `GET /assemblies` (base URL `https://api2.transloadit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-assemblies.md) for the provider-specific parameters and requirements.

