# HubSpot: Batch Read Contacts

Retrieves contacts from HubSpot in a batch.

```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/batch-read-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/batch-read-contacts?connectionId=$CONNECTION_ID&inputs%5B%5D=%5Bobject%20Object%5D&inputs%5B%5D.id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inputs[]": "[object Object]",
  "inputs[].id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/batch-read-contacts?${params}`, {
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
| `inputs[]` | array<object> | yes | The list of contact identifiers to read. |
| `inputs[].id` | string | yes | A contact record ID or unique property value. |
| `properties[]` | array<string> | no | Contact properties to include in the response. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `propertiesWithHistory[]` | array<string> | no | Contact properties to return with value history. |
| `idProperty` | string | no | The unique property to use instead of the default record ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "properties": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the contact is archived. |
| `createdAt` | date | When the contact was created. |
| `id` | string | The contact record ID. |
| `properties` | object | The returned contact properties. |
| `updatedAt` | date | When the contact was last updated. |
| `url` | string | The HubSpot record URL. |

## Native endpoint

Through the native HubSpot API, this operation is `POST crm/v3/objects/contacts/batch/read` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-read-contacts.md) for the provider-specific parameters and requirements.

