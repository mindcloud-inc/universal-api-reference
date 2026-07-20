# PassKit Membership: List Programs

Retrieves membership programs from PassKit Membership.

```
GET https://connect.mindcloud.co/v1/universal/passKitMembership/latest/actions/list-programs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Membership `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passKitMembership/latest/actions/list-programs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passKitMembership/latest/actions/list-programs?${params}`, {
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
      "created": "string",
      "id": "string",
      "localizedName": "Ava Chen",
      "name": "Ava Chen",
      "passTypeIdentifier": "string",
      "profileImageSettings": "string",
      "status": [
        "string"
      ],
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string | Program creation timestamp. |
| `id` | string | PassKit membership program identifier. |
| `localizedName` | string |  |
| `name` | string | Program name. |
| `passTypeIdentifier` | string |  |
| `profileImageSettings` | string |  |
| `status` | array<string> | Program/project status flags. |
| `updated` | string |  |

## Native endpoint

Through the native PassKit Membership API, this operation is `POST /members/programs/list` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-programs.md) for the provider-specific parameters and requirements.

