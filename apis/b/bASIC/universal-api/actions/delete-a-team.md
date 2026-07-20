# BASIC: Delete a team

Deletes an existing team from BASIC.

```
DELETE https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/delete-a-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BASIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/delete-a-team?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/delete-a-team?${params}`, {
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native BASIC API, this operation is `DELETE /team/{team_id}` (base URL `https://api.basic.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-a-team.md) for the provider-specific parameters and requirements.

