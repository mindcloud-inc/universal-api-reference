# Agilite: Get Role

Retrieves responsible users from Agilite by role and conditional level.

```
GET https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agilite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-role?connectionId=$CONNECTION_ID&roleNames=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "roleNames": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-role?${params}`, {
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
| `roleNames` | string | yes | Role name(s) to query, separated by commas when using multiple roles. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conditionalLevels` | string | no | Optional conditional levels for role lookup. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "responsibleUsers": [
        "string"
      ],
      "roleIds": [
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
| `responsibleUsers` | array<string> | Responsible users returned for the requested roles. |
| `roleIds` | array<string> | Role IDs returned for the requested role names. |

## Native endpoint

Through the native Agilite API, this operation is `POST /roles/getRole` (base URL `https://api.agilite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-role.md) for the provider-specific parameters and requirements.

