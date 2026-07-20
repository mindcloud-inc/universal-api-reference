# Postalytics: Get Suppression List

Retrieves a suppression list from Postalytics.

```
GET https://connect.mindcloud.co/v1/universal/postalytics/latest/actions/get-suppression-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postalytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postalytics/latest/actions/get-suppression-list?connectionId=$CONNECTION_ID&id=7654" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "7654"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postalytics/latest/actions/get-suppression-list?${params}`, {
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
| `id` | number | yes | Suppression list ID. Example: `7654`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Country": "string",
      "CreationDate": "string",
      "Id": 1,
      "Name": "Ava Chen",
      "Total": 1,
      "Type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Country` | string | List country. |
| `CreationDate` | string | Creation timestamp. |
| `Id` | number | Suppression list ID. |
| `Name` | string | Suppression list name. |
| `Total` | number | Suppressed contact count. |
| `Type` | string | Suppression list type. |

## Native endpoint

Through the native Postalytics API, this operation is `GET /api/v1/lists/suppression/:id` (base URL `https://api.postalytics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-suppression-list.md) for the provider-specific parameters and requirements.

