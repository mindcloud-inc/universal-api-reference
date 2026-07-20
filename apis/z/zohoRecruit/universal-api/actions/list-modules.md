# Zoho Recruit: List Modules

Retrieves all modules from Zoho Recruit.

```
GET https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/list-modules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Recruit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/list-modules?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/list-modules?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "apiName": "Ava Chen",
      "apiSupported": true,
      "creatable": true,
      "deletable": true,
      "displayField": {},
      "editable": true,
      "filterSupported": true,
      "id": "string",
      "moduleName": "Ava Chen",
      "parentModule": {},
      "pluralLabel": "string",
      "profiles": [
        {}
      ],
      "singularLabel": "string",
      "viewable": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiName` | string |  |
| `apiSupported` | boolean |  |
| `creatable` | boolean |  |
| `deletable` | boolean |  |
| `displayField` | object |  |
| `editable` | boolean |  |
| `filterSupported` | boolean |  |
| `id` | string |  |
| `moduleName` | string |  |
| `parentModule` | object |  |
| `pluralLabel` | string |  |
| `profiles` | array<object> |  |
| `singularLabel` | string |  |
| `viewable` | boolean |  |

## Native endpoint

Through the native Zoho Recruit API, this operation is `GET /settings/modules` (base URL `https://recruit.zoho.com/recruit/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-modules.md) for the provider-specific parameters and requirements.

