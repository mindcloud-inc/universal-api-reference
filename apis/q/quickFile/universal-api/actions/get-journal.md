# QuickFile: Get Journal



```
GET https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-journal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-journal?connectionId=$CONNECTION_ID&journalReference=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "journalReference": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-journal?${params}`, {
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
| `journalReference` | string | yes | The QuickFile journal reference to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "journalDate": "2026-05-07T12:00:00.000Z",
      "journalReference": "string",
      "totalAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Journal description. |
| `journalDate` | date | Journal posting date. |
| `journalReference` | string | QuickFile journal reference. |
| `totalAmount` | number | Journal total amount. |

## Native endpoint

Through the native QuickFile API, this operation is `POST /journal/get` (base URL `https://api.quickfile.co.uk/1_2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-journal.md) for the provider-specific parameters and requirements.

