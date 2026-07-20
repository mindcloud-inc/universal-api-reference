# GoDial: List Teams

Retrieves a list of teams from GoDial.

```
GET https://connect.mindcloud.co/v1/universal/goDial/latest/actions/team-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoDial `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goDial/latest/actions/team-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goDial/latest/actions/team-list?${params}`, {
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
      "companyId": "string",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | string | Owning company identifier. |
| `createdOn` | date | Team creation timestamp. |
| `id` | string | Team identifier. |
| `name` | string | Team name. |

## Native endpoint

Through the native GoDial API, this operation is `GET /externals/team/list` (base URL `https://enterprise.godial.cc/meta/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/team-list.md) for the provider-specific parameters and requirements.

