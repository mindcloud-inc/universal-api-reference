# Lnk.Bio: List Lnks

Retrieves current Lnks from Lnk.Bio.

```
GET https://connect.mindcloud.co/v1/universal/lnkBio/latest/actions/list-lnks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lnk.Bio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lnkBio/latest/actions/list-lnks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lnkBio/latest/actions/list-lnks?${params}`, {
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
      ],
      "errors": [
        "string"
      ],
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | The Lnks currently published on the profile. |
| `errors` | array<string> | Errors returned by the Lnk.Bio API. |
| `status` | boolean | Whether the list Lnks request succeeded. |

## Native endpoint

Through the native Lnk.Bio API, this operation is `GET /lnk/list` (base URL `https://lnk.bio/oauth/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-lnks.md) for the provider-specific parameters and requirements.

