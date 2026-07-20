# Lnk.Bio: List Lnk Groups

Retrieves Lnk groups from Lnk.Bio.

```
GET https://connect.mindcloud.co/v1/universal/lnkBio/latest/actions/list-lnk-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lnk.Bio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lnkBio/latest/actions/list-lnk-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lnkBio/latest/actions/list-lnk-groups?${params}`, {
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
      "errors": [
        "string"
      ],
      "info": {
        "groups": [
          {}
        ]
      },
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> | Errors returned by the Lnk.Bio API. |
| `info.groups` | array<object> | The groups available on the authenticated Lnk.Bio account. |
| `status` | boolean | Whether the list Groups request succeeded. |

## Native endpoint

Through the native Lnk.Bio API, this operation is `GET /group/list` (base URL `https://lnk.bio/oauth/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-lnk-groups.md) for the provider-specific parameters and requirements.

