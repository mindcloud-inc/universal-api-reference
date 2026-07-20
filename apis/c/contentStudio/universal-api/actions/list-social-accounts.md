# ContentStudio: List Social Accounts

Retrieves social accounts for a workspace from ContentStudio.

```
GET https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/list-social-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContentStudio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/list-social-accounts?connectionId=$CONNECTION_ID&workspace_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspace_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/list-social-accounts?${params}`, {
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
| `page` | number | no | Page number for pagination. |
| `per_page` | number | no | Number of items per page. |
| `platform` | string | no | Filter accounts by platform. |
| `search` | string | no | Search term. |
| `workspace_id` | string | yes | ContentStudio workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountName": "Ava Chen",
      "connectedAt": "2026-05-07T12:00:00.000Z",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "Id": "string",
      "platform": "string",
      "profilePicture": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountName` | string |  |
| `connectedAt` | date |  |
| `expiresAt` | date |  |
| `Id` | string |  |
| `platform` | string |  |
| `profilePicture` | string |  |
| `status` | string |  |

## Native endpoint

Through the native ContentStudio API, this operation is `GET /workspaces/:workspace_id/accounts` (base URL `https://api.contentstudio.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-social-accounts.md) for the provider-specific parameters and requirements.

