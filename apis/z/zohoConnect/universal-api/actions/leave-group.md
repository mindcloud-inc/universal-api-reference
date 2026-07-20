# Zoho Connect: Leave Group

Leaves a group in Zoho Connect.

```
DELETE https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/leave-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/leave-group?connectionId=$CONNECTION_ID&scopeId=string&partitionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scopeId": "string",
  "partitionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/leave-group?${params}`, {
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
| `scopeId` | string | yes | Network ID. |
| `partitionId` | string | yes | Group ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "leaveGroup": {
        "assignAdmin": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `leaveGroup.assignAdmin` | string | Returned when Zoho requires the current admin to assign another admin before leaving. |

## Native endpoint

Through the native Zoho Connect API, this operation is `DELETE /pulse/api/leaveGroup` (base URL `https://connect.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/leave-group.md) for the provider-specific parameters and requirements.

