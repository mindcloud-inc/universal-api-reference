# Deputy: Get Contact

Retrieves a single contact from Deputy.

```
GET https://connect.mindcloud.co/v1/universal/deputy/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deputy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deputy/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deputy/latest/actions/get-contact?${params}`, {
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
| `id` | number | yes | Contact ID from Deputy. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_DPMetaData": {},
      "Created": "2026-05-07T12:00:00.000Z",
      "Email": "ava@example.com",
      "Email1": "ava@example.com",
      "Id": 1,
      "Mobile": "string",
      "Modified": "2026-05-07T12:00:00.000Z",
      "Phone1": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_DPMetaData` | object |  |
| `Created` | date |  |
| `Email` | string |  |
| `Email1` | string |  |
| `Id` | number |  |
| `Mobile` | string |  |
| `Modified` | date |  |
| `Phone1` | string |  |

## Native endpoint

Through the native Deputy API, this operation is `GET /api/v1/resource/Contact/:id` (base URL `https://{{credentials.endpoint}}.deputy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

