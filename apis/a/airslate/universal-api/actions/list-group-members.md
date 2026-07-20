# Airslate: List Group Members

Retrieves group member records from airSlate.

```
GET https://connect.mindcloud.co/v1/universal/airslate/latest/actions/list-group-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airslate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airslate/latest/actions/list-group-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airslate/latest/actions/list-group-members?${params}`, {
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
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `meta` | object |  |

## Native endpoint

Through the native Airslate API, this operation is `GET /organizations/{organization_id}/groups/{group_id}/members` (base URL `https://api.airslate.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-group-members.md) for the provider-specific parameters and requirements.

