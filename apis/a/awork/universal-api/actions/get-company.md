# Awork: Get Company

Retrieves a company from Awork.

```
GET https://connect.mindcloud.co/v1/universal/awork/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Awork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/awork/latest/actions/get-company?connectionId=$CONNECTION_ID&companyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/awork/latest/actions/get-company?${params}`, {
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
| `companyId` | string | yes | The id of the company. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdBy": "string",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "hasImage": true,
      "id": "string",
      "isExternal": true,
      "name": "Ava Chen",
      "projectsCount": 1,
      "projectsInProgressCount": 1,
      "resourceVersion": 1,
      "updatedBy": "string",
      "updatedOn": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy` | string |  |
| `createdOn` | date |  |
| `hasImage` | boolean |  |
| `id` | string |  |
| `isExternal` | boolean |  |
| `name` | string |  |
| `projectsCount` | number |  |
| `projectsInProgressCount` | number |  |
| `resourceVersion` | number |  |
| `updatedBy` | string |  |
| `updatedOn` | date |  |

## Native endpoint

Through the native Awork API, this operation is `GET /companies/:companyId` (base URL `https://api.awork.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

