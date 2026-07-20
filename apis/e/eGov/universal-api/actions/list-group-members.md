# e-Gov: List Group Members

Retrieves group members from e-Gov.

```
GET https://connect.mindcloud.co/v1/universal/eGov/latest/actions/list-group-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a e-Gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGov/latest/actions/list-group-members?connectionId=$CONNECTION_ID&id=gr_0200" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "gr_0200"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGov/latest/actions/list-group-members?${params}`, {
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
| `id` | string | yes | Default: `gr_0200`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `object_type` | string | no |  |
| `capacity` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | array<string> |  |

## Native endpoint

Through the native e-Gov API, this operation is `GET /member_list` (base URL `https://data.e-gov.go.jp/data/api/action`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-group-members.md) for the provider-specific parameters and requirements.

