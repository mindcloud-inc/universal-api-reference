# Kintone: List Apps

Retrieves apps from Kintone.

```
GET https://connect.mindcloud.co/v1/universal/kintone/latest/actions/list-apps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kintone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kintone/latest/actions/list-apps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kintone/latest/actions/list-apps?${params}`, {
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
| `ids` | list<number> | no | Filter by one or more Kintone app IDs. Accepts multiple values as an array. |
| `codes` | list<string> | no | Filter by one or more Kintone app codes. Accepts multiple values as an array. |
| `name` | string | no | Filter by app name prefix. |
| `spaceIds` | list<number> | no | Filter by one or more Kintone space IDs. Accepts multiple values as an array. |
| `limit` | number | no | Maximum number of apps to return. |
| `offset` | number | no | Number of apps to skip before returning results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apps": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apps` | array<object> | List of apps visible to the current user. |

## Native endpoint

Through the native Kintone API, this operation is `GET /apps.json` (base URL `{{credentials.baseUrl}}/k/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-apps.md) for the provider-specific parameters and requirements.

