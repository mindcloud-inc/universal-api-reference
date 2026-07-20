# Implisense: Get Company People

Retrieves company people from Implisense API.

```
GET https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/get-company-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Implisense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/get-company-people?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/get-company-people?${params}`, {
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
| `id` | string | yes | Implisense company identifier, for example DEVFCLQFW054. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "role": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `role` | string |  |

## Native endpoint

Through the native Implisense API, this operation is `GET /companies/:id/people` (base URL `https://german-company-data.p.rapidapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-people.md) for the provider-specific parameters and requirements.

