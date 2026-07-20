# TalentLMS: List Branches

Retrieves branches from a TalentLMS domain.

```
GET https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/list-branches
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentLMS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/list-branches?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/list-branches?${params}`, {
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
| `pageNumber` | number | no | Page number for paginated results. |
| `pageSize` | number | no | Number of records per page (max 100). Default: `10`. |

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

Through the native TalentLMS API, this operation is `GET /branches` (base URL `https://{{credentials.domain}}.talentlms.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-branches.md) for the provider-specific parameters and requirements.

