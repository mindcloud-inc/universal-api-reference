# Postalytics: Create Suppression List

Creates a suppression list in Postalytics.

```
POST https://connect.mindcloud.co/v1/universal/postalytics/latest/actions/create-suppression-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postalytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postalytics/latest/actions/create-suppression-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postalytics/latest/actions/create-suppression-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `country` | string | no | Country code for the list. |
| `name` | string | no | Suppression list name. |

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

Through the native Postalytics API, this operation is `POST /api/v1/lists/suppression` (base URL `https://api.postalytics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-suppression-list.md) for the provider-specific parameters and requirements.

