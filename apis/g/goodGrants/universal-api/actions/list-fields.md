# Good Grants: List fields

Retrieves fields from Good Grants.

```
GET https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/list-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Good Grants `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/list-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/list-fields?${params}`, {
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
| `form` | string | no | Filter fields by form slug. |
| `page` | number | no | Page number greater than 0. |
| `perPage` | number | no | Results per page, between 1 and 100. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applicantReadAccess": true,
      "applicantWriteAccess": true,
      "autoScoring": 1,
      "categories": [
        "string"
      ],
      "categoryCount": "string",
      "conditionalField": {},
      "created": "2026-05-07T12:00:00.000Z",
      "fileTypes": [
        "string"
      ],
      "form": {},
      "helpText": {},
      "hintText": {},
      "label": {},
      "order": 1,
      "protection": "string",
      "required": true,
      "resource": "string",
      "searchable": true,
      "season": {},
      "slug": "string",
      "tab": {},
      "title": {},
      "type": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "visibility": [
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
| `applicantReadAccess` | boolean |  |
| `applicantWriteAccess` | boolean |  |
| `autoScoring` | number |  |
| `categories` | array<string> |  |
| `categoryCount` | string |  |
| `conditionalField` | object |  |
| `created` | date |  |
| `fileTypes` | array<string> |  |
| `form` | object |  |
| `helpText` | object |  |
| `hintText` | object |  |
| `label` | object |  |
| `order` | number |  |
| `protection` | string |  |
| `required` | boolean |  |
| `resource` | string |  |
| `searchable` | boolean |  |
| `season` | object |  |
| `slug` | string |  |
| `tab` | object |  |
| `title` | object |  |
| `type` | string |  |
| `updated` | date |  |
| `visibility` | array<string> |  |

## Native endpoint

Through the native Good Grants API, this operation is `GET field` (base URL `https://api.cr4ce.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fields.md) for the provider-specific parameters and requirements.

