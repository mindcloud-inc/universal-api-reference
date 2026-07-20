# Qntrl: List Profile Permissions

Retrieves profile permissions from Qntrl.

```
GET https://connect.mindcloud.co/v1/universal/qntrl/latest/actions/list-profile-permissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qntrl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qntrl/latest/actions/list-profile-permissions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qntrl/latest/actions/list-profile-permissions?${params}`, {
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
| `org_id` | string | no | Qntrl organization ID. |
| `profile_id` | string | no | Qntrl profile ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customfieldId": "string",
      "permission": "string",
      "profileId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customfieldId` | string |  |
| `permission` | string |  |
| `profileId` | string |  |

## Native endpoint

Through the native Qntrl API, this operation is `GET /[:org_id]/profile/permissions/[:profile_id]` (base URL `https://coreapi.qntrl.com/blueprint/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-profile-permissions.md) for the provider-specific parameters and requirements.

