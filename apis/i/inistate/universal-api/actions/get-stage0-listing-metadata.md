# Inistate: Get Stage0 Listing Metadata

Retrieves Stage0 listing metadata from Inistate.

```
GET https://connect.mindcloud.co/v1/universal/inistate/latest/actions/get-stage0-listing-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Inistate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inistate/latest/actions/get-stage0-listing-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inistate/latest/actions/get-stage0-listing-metadata?${params}`, {
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
      "data": {},
      "header": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Page envelope containing one sample row plus pagination totals. |
| `header` | object | Listing header metadata including columns and standard activities. |

## Native endpoint

Through the native Inistate API, this operation is `POST /api/workspace/list` (base URL `https://api.inistate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stage0-listing-metadata.md) for the provider-specific parameters and requirements.

