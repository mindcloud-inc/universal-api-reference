# Next Cloud OCS: Get Group Members

Retrieves group members from Next Cloud OCS.

```
GET https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/get-group-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Next Cloud OCS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/get-group-members?connectionId=$CONNECTION_ID&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/get-group-members?${params}`, {
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
| `groupId` | string | yes | Nextcloud group ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "element": "string",
      "message": "string",
      "status": "string",
      "users": [
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
| `element` | string |  |
| `message` | string |  |
| `status` | string |  |
| `users` | array<string> |  |

## Native endpoint

Through the native Next Cloud OCS API, this operation is `GET /ocs/v1.php/cloud/groups/{{groupId}}` (base URL `https://demo2.nextcloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group-members.md) for the provider-specific parameters and requirements.

