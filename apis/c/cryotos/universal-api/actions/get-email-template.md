# Cryotos: Get Email Template



```
GET https://connect.mindcloud.co/v1/universal/cryotos/latest/actions/get-email-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryotos `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cryotos/latest/actions/get-email-template?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cryotos/latest/actions/get-email-template?${params}`, {
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
| `id` | string | yes | The email template ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "body": "string",
      "bodyTemplate": "string",
      "creationDate": "string",
      "filterBy": "string",
      "id": 1,
      "moduleName": "Ava Chen",
      "name": "Ava Chen",
      "searchText": "string",
      "subject": "string",
      "toAddresses": [
        "string"
      ],
      "updationDate": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `body` | string |  |
| `bodyTemplate` | string |  |
| `creationDate` | string |  |
| `filterBy` | string |  |
| `id` | number |  |
| `moduleName` | string |  |
| `name` | string |  |
| `searchText` | string |  |
| `subject` | string |  |
| `toAddresses` | array<string> |  |
| `updationDate` | string |  |
| `version` | number |  |

## Native endpoint

Through the native Cryotos API, this operation is `GET /api/email_template/:id` (base URL `https://app.cryotos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-template.md) for the provider-specific parameters and requirements.

