# Hireflix: Get Theme

Retrieves a theme from Hireflix.

```
GET https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/get-theme
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hireflix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/get-theme?connectionId=$CONNECTION_ID&variables.id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/get-theme?${params}`, {
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
| `variables.id` | string | yes | The Hireflix theme ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyName": "Ava Chen",
      "id": "string",
      "name": "Ava Chen",
      "owner": "string",
      "primaryColor": "string",
      "testName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyName` | string |  |
| `id` | string |  |
| `name` | string |  |
| `owner` | string |  |
| `primaryColor` | string |  |
| `testName` | string |  |

## Native endpoint

Through the native Hireflix API, this operation is `POST me` (base URL `https://api.hireflix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-theme.md) for the provider-specific parameters and requirements.

