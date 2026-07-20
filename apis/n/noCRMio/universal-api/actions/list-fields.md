# noCRM.io: List Fields

Retrieves fields from noCRM.io.

```
GET https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/list-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a noCRM.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/list-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/list-fields?${params}`, {
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
| `type` | string | no | Restrict fields to lead or client. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": 1,
      "isKey": "string",
      "name": "Ava Chen",
      "parentType": "string",
      "position": 1,
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | number |  |
| `isKey` | string |  |
| `name` | string |  |
| `parentType` | string |  |
| `position` | number |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native noCRM.io API, this operation is `GET /fields` (base URL `{{credentials.baseUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fields.md) for the provider-specific parameters and requirements.

