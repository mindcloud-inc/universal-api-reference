# WorkAdventure: List members

Retrieves members from a WorkAdventure world.

```
GET https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/list-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkAdventure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/list-members?connectionId=$CONNECTION_ID&worldSlug=string&limit=10&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "worldSlug": "string",
  "limit": "10",
  "offset": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/list-members?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `worldSlug` | string | yes | The world slug from the WorkAdventure world URL. |
| `limit` | number | yes | Maximum number of records to return. The API requires this query parameter and allows up to 100. Default: `10`. |
| `offset` | number | yes | Offset of the records returned. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `total` | number |  |

## Native endpoint

Through the native WorkAdventure API, this operation is `GET /api/v1/worlds/:worldSlug/members` (base URL `https://admin.workadventu.re`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-members.md) for the provider-specific parameters and requirements.

