# Damstra Forms: Get Punch List

Retrieves a punch list from Damstra Forms.

```
GET https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/get-punch-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Damstra Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/get-punch-list?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/get-punch-list?${params}`, {
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
| `id` | number | yes | The unique identifier of the punch list. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientCreatedAt": "2026-05-07T12:00:00.000Z",
      "clientUpdatedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdByUserId": 1,
      "draftTemplateId": 1,
      "id": 1,
      "name": "Ava Chen",
      "ownedByUserId": 1,
      "projectId": 1,
      "status": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientCreatedAt` | date | From Damstra Forms API example response. |
| `clientUpdatedAt` | date | From Damstra Forms API example response. |
| `createdAt` | date | From Damstra Forms API example response. |
| `createdByUserId` | number | From Damstra Forms API example response. |
| `draftTemplateId` | number | From Damstra Forms API example response. |
| `id` | number | From Damstra Forms API example response. |
| `name` | string | From Damstra Forms API example response. |
| `ownedByUserId` | number | From Damstra Forms API example response. |
| `projectId` | number | From Damstra Forms API example response. |
| `status` | number | From Damstra Forms API example response. |
| `updatedAt` | date | From Damstra Forms API example response. |

## Native endpoint

Through the native Damstra Forms API, this operation is `GET /punch_lists/{id}` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-punch-list.md) for the provider-specific parameters and requirements.

