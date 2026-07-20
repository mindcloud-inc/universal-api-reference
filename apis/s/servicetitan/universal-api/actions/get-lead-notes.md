# ServiceTitan: Get Lead Notes

Retrieves lead notes from ServiceTitan.

```
GET https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-lead-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-lead-notes?connectionId=$CONNECTION_ID&leadId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "leadId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-lead-notes?${params}`, {
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
| `leadId` | string | yes |  |
| `createdBefore` | string | no |  |
| `createdOnOrAfter` | string | no |  |
| `modifiedBefore` | string | no |  |
| `modifiedOnOrAfter` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdById": 1,
      "createdOn": "string",
      "id": 1,
      "isPinned": true,
      "modifiedOn": "string",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdById` | number |  |
| `createdOn` | string |  |
| `id` | number |  |
| `isPinned` | boolean |  |
| `modifiedOn` | string |  |
| `text` | string |  |

## Native endpoint

Through the native ServiceTitan API, this operation is `GET crm/v2/tenant/{{credentials.tenant}}/leads/:leadId/notes` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lead-notes.md) for the provider-specific parameters and requirements.

