# SquareSpace: List Profiles

Retrieves customer profiles from Squarespace.

```
GET https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/list-profiles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SquareSpace `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/list-profiles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/list-profiles?${params}`, {
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
      "pagination": {},
      "profiles": [
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
| `pagination` | object | Pagination metadata. |
| `profiles` | array<object> | Profile rows. |

## Native endpoint

Through the native SquareSpace API, this operation is `GET /1.0/profiles` (base URL `https://api.squarespace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-profiles.md) for the provider-specific parameters and requirements.

