# AidaForm: List Forms

Retrieves forms from your AidaForm account.

```
GET https://connect.mindcloud.co/v1/universal/aidaForm/latest/actions/list-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AidaForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aidaForm/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aidaForm/latest/actions/list-forms?${params}`, {
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
      "count": 1,
      "items": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "dashboardToken": {},
          "data": {
            "backgroundWidth": 1,
            "code": "string",
            "language": "string",
            "name": "Ava Chen",
            "notificationsEnabled": true,
            "submit": {
              "label": "string",
              "prevLabel": "string"
            },
            "theme": "string"
          },
          "domain": "string",
          "fields": [
            {
              "id": "string",
              "label": "string",
              "properties": {
                "align": "string",
                "firstName": "Ava",
                "lastName": "Chen",
                "placeholderFirstName": "Ava",
                "placeholderLastName": "Chen",
                "required": true
              },
              "type": "string"
            }
          ],
          "id": "string",
          "inventory": {},
          "owner": "string",
          "responses": 1,
          "shareToken": {},
          "shareTokenCreated": {},
          "status": "string",
          "unread": 1,
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "uri": "string",
          "version": 1,
          "views": 1
        }
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `items[].createdAt` | date |  |
| `items[].dashboardToken` | object |  |
| `items[].data.backgroundWidth` | number |  |
| `items[].data.code` | string |  |
| `items[].data.language` | string |  |
| `items[].data.name` | string |  |
| `items[].data.notificationsEnabled` | boolean |  |
| `items[].data.submit.label` | string |  |
| `items[].data.submit.prevLabel` | string |  |
| `items[].data.theme` | string |  |
| `items[].domain` | string |  |
| `items[].fields[].id` | string |  |
| `items[].fields[].label` | string |  |
| `items[].fields[].properties.align` | string |  |
| `items[].fields[].properties.firstName` | string |  |
| `items[].fields[].properties.lastName` | string |  |
| `items[].fields[].properties.placeholderFirstName` | string |  |
| `items[].fields[].properties.placeholderLastName` | string |  |
| `items[].fields[].properties.required` | boolean |  |
| `items[].fields[].type` | string |  |
| `items[].id` | string |  |
| `items[].inventory` | object |  |
| `items[].owner` | string |  |
| `items[].responses` | number |  |
| `items[].shareToken` | object |  |
| `items[].shareTokenCreated` | object |  |
| `items[].status` | string |  |
| `items[].unread` | number |  |
| `items[].updatedAt` | date |  |
| `items[].uri` | string |  |
| `items[].version` | number |  |
| `items[].views` | number |  |
| `total` | number |  |

## Native endpoint

Through the native AidaForm API, this operation is `GET /forms` (base URL `https://api.aidaform.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-forms.md) for the provider-specific parameters and requirements.

