# TalentLMS: Get Branch

Retrieves a branch from a TalentLMS domain.

```
GET https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/get-branch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentLMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/get-branch?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/get-branch?${params}`, {
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
| `id` | number | yes | Numeric branch ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "defaultGroup": {},
      "defaultLocale": "string",
      "defaultTimezone": "string",
      "defaultUserType": {},
      "description": "string",
      "ecommerce": {},
      "id": 1,
      "name": "Ava Chen",
      "ownerId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `defaultGroup` | object |  |
| `defaultLocale` | string |  |
| `defaultTimezone` | string |  |
| `defaultUserType` | object |  |
| `description` | string |  |
| `ecommerce` | object |  |
| `id` | number |  |
| `name` | string |  |
| `ownerId` | number |  |

## Native endpoint

Through the native TalentLMS API, this operation is `GET /branches/:id` (base URL `https://{{credentials.domain}}.talentlms.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-branch.md) for the provider-specific parameters and requirements.

