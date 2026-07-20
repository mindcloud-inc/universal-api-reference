# CompanyHub: Delete Records

Deletes one or more records from a CompanyHub table.

```
DELETE https://connect.mindcloud.co/v1/universal/companyHub/latest/actions/delete-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CompanyHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/companyHub/latest/actions/delete-records?connectionId=$CONNECTION_ID&tableName=Contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tableName": "Contact"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companyHub/latest/actions/delete-records?${params}`, {
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
| `tableName` | string | yes | Exact CompanyHub API table name, for example Contact, Company, Deal, or a custom table name. Example: `Contact`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native CompanyHub API, this operation is `DELETE /tables/:tableName` (base URL `https://api.companyhub.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-records.md) for the provider-specific parameters and requirements.

