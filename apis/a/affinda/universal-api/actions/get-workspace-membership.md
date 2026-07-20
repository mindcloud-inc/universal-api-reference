# Affinda: Get specific workspace membership

Retrieves a specific workspace membership from Affinda.

```
GET https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-workspace-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Affinda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-workspace-membership?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-workspace-membership?${params}`, {
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
| `identifier` | string | yes | Workspace membership's identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "identifier": "string",
      "user": {},
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `identifier` | string |  |
| `user` | object |  |
| `workspace` | string |  |

## Native endpoint

Through the native Affinda API, this operation is `GET /v3/workspace_memberships/:identifier` (base URL `https://api.us1.affinda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace-membership.md) for the provider-specific parameters and requirements.

