# OneDesk: Get Project By External ID

Retrieves a project by external ID from OneDesk.

```
GET https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/get-project-by-external-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/get-project-by-external-id?connectionId=$CONNECTION_ID&externalId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "externalId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/get-project-by-external-id?${params}`, {
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
| `externalId` | string | yes | External ID of the project. |

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

Through the native OneDesk API, this operation is `GET /rest/public/projects/externalId/:externalId` (base URL `https://app.onedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-by-external-id.md) for the provider-specific parameters and requirements.

