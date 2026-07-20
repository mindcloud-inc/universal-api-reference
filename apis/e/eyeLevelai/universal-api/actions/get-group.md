# EyeLevel.ai: Get Group

Retrieves a group from EyeLevel.ai.

```
GET https://connect.mindcloud.co/v1/universal/eyeLevelai/latest/actions/get-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EyeLevel.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eyeLevelai/latest/actions/get-group?connectionId=$CONNECTION_ID&groupId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eyeLevelai/latest/actions/get-group?${params}`, {
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
| `groupId` | number | yes | The groupId of the group to look up. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "group": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `group` | object | The requested group. |

## Native endpoint

Through the native EyeLevel.ai API, this operation is `GET /group/:groupId` (base URL `https://api.groundx.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group.md) for the provider-specific parameters and requirements.

