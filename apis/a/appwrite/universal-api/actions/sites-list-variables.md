# Appwrite: List variables

Retrieves a list of variables from your Appwrite project.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/sites-list-variables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/sites-list-variables?connectionId=$CONNECTION_ID&siteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/sites-list-variables?${params}`, {
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
| `siteId` | string | yes | Site unique ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "total": 1,
      "variables": [
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
| `total` | number | Total number of variables that matched your query. |
| `variables` | array<object> | List of variables. |

## Native endpoint

Through the native Appwrite API, this operation is `GET /sites/{siteId}/variables` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sites-list-variables.md) for the provider-specific parameters and requirements.

