# folk: Delete Company

Deletes an existing company from folk.

```
DELETE https://connect.mindcloud.co/v1/universal/folk/latest/actions/delete-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a folk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/folk/latest/actions/delete-company?connectionId=$CONNECTION_ID&companyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/folk/latest/actions/delete-company?${params}`, {
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
| `companyId` | string | yes | The ID of the company to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native folk API, this operation is `DELETE /v1/companies/:companyId` (base URL `https://api.folk.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-company.md) for the provider-specific parameters and requirements.

