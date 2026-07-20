# Pabbly Hook: Get All Transformations



```
GET https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/get-all-transformations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Hook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/get-all-transformations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/get-all-transformations?${params}`, {
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
      "Id": "string",
      "name": "Ava Chen",
      "trsId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Id` | string | Pabbly Hook internal transformation identifier. |
| `name` | string | Transformation name. |
| `trsId` | string | Public Pabbly Hook transformation identifier. |

## Native endpoint

Through the native Pabbly Hook API, this operation is `GET /api/v1/transformations/get-all/` (base URL `https://hook.pabbly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-transformations.md) for the provider-specific parameters and requirements.

