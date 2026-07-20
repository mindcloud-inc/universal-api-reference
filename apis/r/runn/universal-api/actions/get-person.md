# Runn: Get Person



```
GET https://connect.mindcloud.co/v1/universal/runn/latest/actions/get-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runn/latest/actions/get-person?connectionId=$CONNECTION_ID&personId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "personId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runn/latest/actions/get-person?${params}`, {
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
| `personId` | number | yes | Runn person ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "firstName": "Ava",
      "id": 1,
      "isArchived": true,
      "lastName": "Chen",
      "teamId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `firstName` | string | Person first name. |
| `id` | number | Person ID. |
| `isArchived` | boolean | Whether the person is archived. |
| `lastName` | string | Person last name. |
| `teamId` | number | Current team ID. |

## Native endpoint

Through the native Runn API, this operation is `GET /people/{{personId}}` (base URL `https://api.runn.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person.md) for the provider-specific parameters and requirements.

