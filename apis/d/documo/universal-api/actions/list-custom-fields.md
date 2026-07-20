# Documo: List Custom Fields

Retrieves custom field records from Documo.

```
GET https://connect.mindcloud.co/v1/universal/documo/latest/actions/list-custom-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documo/latest/actions/list-custom-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documo/latest/actions/list-custom-fields?${params}`, {
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
| `entity` | string | no | Entity type to filter by. Possible values: fax, account, user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiName": "Ava Chen",
      "archivedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "displayUI": true,
      "displayUITable": true,
      "entity": "string",
      "hint": "string",
      "isArchived": true,
      "label": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiName` | string |  |
| `archivedAt` | date |  |
| `createdAt` | date |  |
| `displayUI` | boolean |  |
| `displayUITable` | boolean |  |
| `entity` | string |  |
| `hint` | string |  |
| `isArchived` | boolean |  |
| `label` | string |  |
| `updatedAt` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Documo API, this operation is `GET /v1/custom-fields` (base URL `https://api.documo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-fields.md) for the provider-specific parameters and requirements.

