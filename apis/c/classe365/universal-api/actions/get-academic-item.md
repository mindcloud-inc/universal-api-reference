# Classe365: Get Academic Item

Retrieves an academic item from Classe365 by type and ID.

```
GET https://connect.mindcloud.co/v1/universal/classe365/latest/actions/get-academic-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Classe365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/classe365/latest/actions/get-academic-item?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/classe365/latest/actions/get-academic-item?${params}`, {
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
| `id` | string | no | Academic entity id to fetch. |
| `type` | string | no | Entity type such as class, section, or subject. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "classCode": "string",
      "classId": "string",
      "className": "Ava Chen",
      "departmentId": 1,
      "departmentName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `classCode` | string |  |
| `classId` | string |  |
| `className` | string |  |
| `departmentId` | number |  |
| `departmentName` | string |  |

## Native endpoint

Through the native Classe365 API, this operation is `GET /rest/getAcademicDataForParticular` (base URL `https://{{credentials.username}}.classe365.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-academic-item.md) for the provider-specific parameters and requirements.

