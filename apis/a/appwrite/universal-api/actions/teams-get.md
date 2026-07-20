# Appwrite: Get team

Retrieves team details from your Appwrite project.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/teams-get
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/teams-get?connectionId=$CONNECTION_ID&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/teams-get?${params}`, {
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
| `teamId` | string | yes | Team ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$createdAt": "string",
      "$id": "string",
      "$updatedAt": "string",
      "name": "Ava Chen",
      "prefs": {},
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$createdAt` | string | Team creation date in ISO 8601 format. |
| `$id` | string | Team ID. |
| `$updatedAt` | string | Team update date in ISO 8601 format. |
| `name` | string | Team name. |
| `prefs` | object | Team preferences as a key-value object |
| `total` | number | Total number of team members. |

## Native endpoint

Through the native Appwrite API, this operation is `GET /teams/{teamId}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/teams-get.md) for the provider-specific parameters and requirements.

