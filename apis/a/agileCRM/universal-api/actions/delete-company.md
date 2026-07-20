# Agile CRM: Delete Company

Deletes an existing company from Agile CRM.

```
DELETE https://connect.mindcloud.co/v1/universal/agileCRM/latest/actions/delete-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agile CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/agileCRM/latest/actions/delete-company?connectionId=$CONNECTION_ID&companyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agileCRM/latest/actions/delete-company?${params}`, {
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
| `companyId` | list | yes | Company record to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | string | Deleted company identifier. |

## Native endpoint

Through the native Agile CRM API, this operation is `DELETE /contacts/{{companyId}}` (base URL `https://mindcloud.agilecrm.com/dev/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-company.md) for the provider-specific parameters and requirements.

