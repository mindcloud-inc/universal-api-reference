# Socket: Get Repository Label

Retrieves a repository label from Socket.

```
GET https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-repository-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-repository-label?connectionId=$CONNECTION_ID&labelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "labelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-repository-label?${params}`, {
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
| `labelId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hasLicensePolicy": true,
      "hasSecurityPolicy": true,
      "id": "string",
      "name": "Ava Chen",
      "repositoryIds": [
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
| `hasLicensePolicy` | boolean | Whether the label has a license policy |
| `hasSecurityPolicy` | boolean | Whether the label has a security policy |
| `id` | string | The ID of the label |
| `name` | string | The name of the label |
| `repositoryIds` | array<string> |  |

## Native endpoint

Through the native Socket API, this operation is `GET /orgs/:org_slug/repos/labels/:label_id` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-repository-label.md) for the provider-specific parameters and requirements.

