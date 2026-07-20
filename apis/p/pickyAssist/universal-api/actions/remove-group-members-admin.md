# Picky Assist: Remove Group Members / Admin



```
DELETE https://connect.mindcloud.co/v1/universal/pickyAssist/latest/actions/remove-group-members-admin
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Picky Assist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pickyAssist/latest/actions/remove-group-members-admin?connectionId=$CONNECTION_ID&group_id=string&type=1&number%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "group_id": "string",
  "type": "1",
  "number[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pickyAssist/latest/actions/remove-group-members-admin?${params}`, {
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
| `group_id` | string | yes |  |
| `type` | number | yes |  |
| `number[]` | array<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | number |  |

## Native endpoint

Through the native Picky Assist API, this operation is `POST /remove-group-members` (base URL `https://app.pickyassist.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-group-members-admin.md) for the provider-specific parameters and requirements.

