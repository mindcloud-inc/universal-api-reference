# Favro: Get Column

Retrieves a column from Favro by column ID.

```
GET https://connect.mindcloud.co/v1/universal/favro/latest/actions/get-column
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Favro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/favro/latest/actions/get-column?connectionId=$CONNECTION_ID&columnId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "columnId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/favro/latest/actions/get-column?${params}`, {
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
| `columnId` | string | yes | The Favro column ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cardCount": 1,
      "columnId": "string",
      "estimationSum": 1,
      "name": "Ava Chen",
      "organizationId": "string",
      "position": 1,
      "timeSum": 1,
      "widgetCommonId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cardCount` | number |  |
| `columnId` | string |  |
| `estimationSum` | number |  |
| `name` | string |  |
| `organizationId` | string |  |
| `position` | number |  |
| `timeSum` | number |  |
| `widgetCommonId` | string |  |

## Native endpoint

Through the native Favro API, this operation is `GET /columns/:columnId` (base URL `https://favro.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-column.md) for the provider-specific parameters and requirements.

