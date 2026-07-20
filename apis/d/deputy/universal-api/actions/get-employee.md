# Deputy: Get Employee

Retrieves a single employee from Deputy.

```
GET https://connect.mindcloud.co/v1/universal/deputy/latest/actions/get-employee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deputy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deputy/latest/actions/get-employee?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deputy/latest/actions/get-employee?${params}`, {
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
| `id` | number | yes | Employee ID from Deputy. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_DPMetaData": {},
      "Active": true,
      "Contact": 1,
      "Created": "2026-05-07T12:00:00.000Z",
      "DisplayName": "Ava Chen",
      "FirstName": "Ava",
      "Id": 1,
      "LastName": "Chen",
      "Modified": "2026-05-07T12:00:00.000Z",
      "StartDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_DPMetaData` | object |  |
| `Active` | boolean |  |
| `Contact` | number |  |
| `Created` | date |  |
| `DisplayName` | string |  |
| `FirstName` | string |  |
| `Id` | number |  |
| `LastName` | string |  |
| `Modified` | date |  |
| `StartDate` | date |  |

## Native endpoint

Through the native Deputy API, this operation is `GET /api/v1/resource/Employee/:id` (base URL `https://{{credentials.endpoint}}.deputy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-employee.md) for the provider-specific parameters and requirements.

