# RD Station CRM: Get Contact

Retrieves contact details from RD Station CRM.

```
GET https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RD Station CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/get-contact?${params}`, {
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
| `id` | string | yes | Contact identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "contextOrigin": "string",
        "createdAt": "string",
        "customFields": {},
        "emails": [
          [
            {}
          ]
        ],
        "id": "string",
        "legalBases": [
          [
            "string"
          ]
        ],
        "name": "Ava Chen",
        "phones": [
          [
            {}
          ]
        ],
        "socialProfiles": [
          [
            "string"
          ]
        ],
        "updatedAt": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.contextOrigin` | string |  |
| `data.createdAt` | string |  |
| `data.customFields` | object |  |
| `data.emails[]` | array<object> |  |
| `data.emails[].email` | string |  |
| `data.id` | string |  |
| `data.legalBases[]` | array<string> |  |
| `data.name` | string |  |
| `data.phones[]` | array<object> |  |
| `data.phones[].phone` | string |  |
| `data.socialProfiles[]` | array<string> |  |
| `data.updatedAt` | string |  |

## Native endpoint

Through the native RD Station CRM API, this operation is `GET /contacts/:id` (base URL `https://api.rd.services/crm/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

