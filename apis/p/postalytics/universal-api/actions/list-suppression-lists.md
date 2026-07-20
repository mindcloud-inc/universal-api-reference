# Postalytics: List Suppression Lists

Retrieves suppression lists from Postalytics.

```
GET https://connect.mindcloud.co/v1/universal/postalytics/latest/actions/list-suppression-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postalytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postalytics/latest/actions/list-suppression-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postalytics/latest/actions/list-suppression-lists?${params}`, {
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
| `id` | number | no | Suppression list ID. |

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

Through the native Postalytics API, this operation is `GET /api/v1/lists/suppression` (base URL `https://api.postalytics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-suppression-lists.md) for the provider-specific parameters and requirements.

