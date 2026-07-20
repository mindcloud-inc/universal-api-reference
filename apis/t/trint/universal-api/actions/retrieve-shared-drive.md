# Trint: Retrieve Shared Drive

Retrieves a shared drive from your Trint account.

```
GET https://connect.mindcloud.co/v1/universal/trint/latest/actions/retrieve-shared-drive
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trint/latest/actions/retrieve-shared-drive?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trint/latest/actions/retrieve-shared-drive?${params}`, {
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
| `workspaceId` | string | yes | The shared drive identifier to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string | Shared drive name. |
| `workspaceId` | string | Shared drive identifier. |

## Native endpoint

Through the native Trint API, this operation is `GET /workspaces/workspace` (base URL `https://api.trint.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-shared-drive.md) for the provider-specific parameters and requirements.

