# Filestage: List Mention Suggestions

Retrieves mention suggestions from Filestage.

```
GET https://connect.mindcloud.co/v1/universal/filestage/latest/actions/list-mention-suggestions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Filestage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filestage/latest/actions/list-mention-suggestions?connectionId=$CONNECTION_ID&stepId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stepId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filestage/latest/actions/list-mention-suggestions?${params}`, {
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
| `stepId` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `isTeamOnlyComment` | boolean | no | Should suggest only reviewers and team members with access to the project Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "fullName": "Ava Chen",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string |  |
| `email` | string |  |
| `fullName` | string |  |
| `id` | string |  |

## Native endpoint

Through the native Filestage API, this operation is `GET /steps/{stepId}/mention-suggestions` (base URL `https://api.filestage.io/ext/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-mention-suggestions.md) for the provider-specific parameters and requirements.

