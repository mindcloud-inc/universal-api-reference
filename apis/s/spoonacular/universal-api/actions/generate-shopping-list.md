# Spoonacular: Generate Shopping List

Generates a shopping list in Spoonacular.

```
GET https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/generate-shopping-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/generate-shopping-list?connectionId=$CONNECTION_ID&endDate=string&hash=string&startDate=string&username=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "endDate": "string",
  "hash": "string",
  "startDate": "string",
  "username": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/generate-shopping-list?${params}`, {
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
| `endDate` | string | yes | Required by the Spoonacular endpoint. |
| `hash` | string | yes | Required by the Spoonacular endpoint. |
| `startDate` | string | yes | Required by the Spoonacular endpoint. |
| `username` | string | yes | Required by the Spoonacular endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |

## Native endpoint

Through the native Spoonacular API, this operation is `POST /mealplanner/{username}/shopping-list/{start-date}/{end-date}` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-shopping-list.md) for the provider-specific parameters and requirements.

