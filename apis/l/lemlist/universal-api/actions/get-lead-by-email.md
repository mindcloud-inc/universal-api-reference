# lemlist: Get Lead by Email

Finds a lead in lemlist by email address.

```
GET https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/get-lead-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a lemlist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/get-lead-by-email?connectionId=$CONNECTION_ID&email=jane.doe%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "jane.doe@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/get-lead-by-email?${params}`, {
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
| `email` | string | yes | The email address of the lead to retrieve. Example: `jane.doe@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign": {
        "id": "string",
        "name": "Ava Chen",
        "status": "string"
      },
      "contactId": "string",
      "enrichment": {},
      "id": "string",
      "isPaused": true,
      "personalized": true,
      "sendingUser": {},
      "source": "string",
      "state": "string",
      "status": "string",
      "updatedAt": "string",
      "variables": {
        "companyName": "Ava Chen",
        "email": "ava@example.com",
        "firstName": "Ava",
        "jobTitle": "string",
        "lastName": "Chen",
        "phone": "string",
        "preferredContactMethod": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign` | object |  |
| `campaign.id` | string |  |
| `campaign.name` | string |  |
| `campaign.status` | string |  |
| `contactId` | string |  |
| `enrichment` | object |  |
| `id` | string |  |
| `isPaused` | boolean |  |
| `personalized` | boolean |  |
| `sendingUser` | object |  |
| `source` | string |  |
| `state` | string |  |
| `status` | string |  |
| `updatedAt` | string |  |
| `variables` | object |  |
| `variables.companyName` | string |  |
| `variables.email` | string |  |
| `variables.firstName` | string |  |
| `variables.jobTitle` | string |  |
| `variables.lastName` | string |  |
| `variables.phone` | string |  |
| `variables.preferredContactMethod` | string |  |

## Native endpoint

Through the native lemlist API, this operation is `GET /leads/:email` (base URL `https://api.lemlist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lead-by-email.md) for the provider-specific parameters and requirements.

