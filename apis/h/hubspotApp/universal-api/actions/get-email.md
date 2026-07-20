# HubSpot: Get Email

Retrieves an email activity from HubSpot by ID.

```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/get-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/get-email?connectionId=$CONNECTION_ID&emailId=123456789" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emailId": "123456789"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/get-email?${params}`, {
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
| `emailId` | string | yes | The email record ID or unique property value when used with idProperty. Example: `123456789`. |
| `properties[]` | array<string> | no | A list of properties to return. Example: `hs_email_subject`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `propertiesWithHistory[]` | array<string> | no | A list of properties to return with history. Example: `hs_email_subject`. |
| `associations[]` | array<string> | no | A list of associated object types to retrieve. Example: `contact`. |
| `idProperty` | string | no | The name of a unique property to use instead of the record ID. Example: `hs_object_id`. |
| `archived` | boolean | no | Whether to include archived records. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "associations": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "properties": {},
      "propertiesWithHistory": {},
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the email is archived. |
| `associations` | object | Associated object IDs returned when requested. |
| `createdAt` | date | When the email was created. |
| `id` | string | The email record ID. |
| `properties` | object | The returned email properties. |
| `propertiesWithHistory` | object | Returned email properties with history when requested. |
| `updatedAt` | date | When the email was last updated. |

## Native endpoint

Through the native HubSpot API, this operation is `GET crm/v3/objects/emails/:emailId` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email.md) for the provider-specific parameters and requirements.

