# OneDesk: Search Projects With Details

Finds projects in OneDesk by filters, with details.

```
GET https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/search-projects-with-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/search-projects-with-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/search-projects-with-details?${params}`, {
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
| `properties[]` | array<object> | no | Array of OneDesk property filters. |
| `properties[].operation` | string | no | Comparison operation to apply to the property. |
| `properties[].property` | string | no | Name of property to be filtered. |
| `properties[].value` | string | no | Value used in the filter comparison. |
| `limit` | number | no | Maximum number of project detail rows to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "archivedDate": "2026-05-07T12:00:00.000Z",
      "author": {
        "displayName": "Ava Chen",
        "email": "ava@example.com",
        "externalId": "string",
        "teamName": {},
        "typeName": "Ava Chen"
      },
      "created": "2026-05-07T12:00:00.000Z",
      "description": {},
      "discoverable": true,
      "externalId": "string",
      "id": 1,
      "invoiceType": "string",
      "lifecycleStatus": {
        "externalId": "string",
        "name": "Ava Chen",
        "state": "string"
      },
      "name": "Ava Chen",
      "published": true,
      "requesterCustomerOrganization": {},
      "template": true,
      "type": {
        "label": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `archivedDate` | date |  |
| `author.displayName` | string |  |
| `author.email` | string |  |
| `author.externalId` | string |  |
| `author.teamName` | object |  |
| `author.typeName` | string |  |
| `created` | date |  |
| `description` | object |  |
| `discoverable` | boolean |  |
| `externalId` | string |  |
| `id` | number |  |
| `invoiceType` | string |  |
| `lifecycleStatus.externalId` | string |  |
| `lifecycleStatus.name` | string |  |
| `lifecycleStatus.state` | string |  |
| `name` | string |  |
| `published` | boolean |  |
| `requesterCustomerOrganization` | object |  |
| `template` | boolean |  |
| `type.label` | string |  |

## Native endpoint

Through the native OneDesk API, this operation is `POST /rest/public/projects/filter/details` (base URL `https://app.onedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-projects-with-details.md) for the provider-specific parameters and requirements.

