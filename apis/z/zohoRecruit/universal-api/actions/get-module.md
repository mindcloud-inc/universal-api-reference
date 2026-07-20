# Zoho Recruit: Get Module

Retrieves a module from Zoho Recruit.

```
GET https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/get-module
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Recruit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/get-module?connectionId=$CONNECTION_ID&moduleApiName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "moduleApiName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/get-module?${params}`, {
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
| `moduleApiName` | string | yes | The Zoho Recruit module API name, for example Candidates or Job_Openings. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiName": "Ava Chen",
      "apiSupported": true,
      "attachmenttypes": [
        {}
      ],
      "creatable": true,
      "customView": {},
      "deletable": true,
      "displayField": {},
      "editable": true,
      "filterSupported": true,
      "id": "string",
      "moduleName": "Ava Chen",
      "parentModule": {},
      "perPage": 1,
      "pluralLabel": "string",
      "profiles": [
        {}
      ],
      "relatedListProperties": {},
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
| `attachmenttypes` | array<object> |  |
| `creatable` | boolean |  |
| `customView` | object |  |
| `deletable` | boolean |  |
| `displayField` | object |  |
| `editable` | boolean |  |
| `filterSupported` | boolean |  |
| `id` | string |  |
| `moduleName` | string |  |
| `parentModule` | object |  |
| `perPage` | number |  |
| `pluralLabel` | string |  |
| `profiles` | array<object> |  |
| `relatedListProperties` | object |  |
| `singularLabel` | string |  |
| `viewable` | boolean |  |

## Native endpoint

Through the native Zoho Recruit API, this operation is `GET /settings/modules/:moduleApiName` (base URL `https://recruit.zoho.com/recruit/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-module.md) for the provider-specific parameters and requirements.

