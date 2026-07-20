# AITable.ai: Get Member

Retrieves a member from a space in AITable.ai.

```
GET https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/get-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AITable.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/get-member?connectionId=$CONNECTION_ID&spaceId=string&unitId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "spaceId": "string",
  "unitId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/get-member?${params}`, {
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
| `spaceId` | string | yes | AITable space ID containing the member. |
| `unitId` | string | yes | AITable member unit ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar": "string",
      "name": "Ava Chen",
      "unitId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | string | Member avatar URL. |
| `name` | string | Member name. |
| `unitId` | string | Member unit ID. |

## Native endpoint

Through the native AITable.ai API, this operation is `GET /fusion/v1/spaces/:spaceId/members/:unitId` (base URL `https://aitable.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-member.md) for the provider-specific parameters and requirements.

