# Airzone Cloud: List Installations

Retrieves confirmed user installations from Airzone Cloud.

```
GET https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/list-installations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airzone Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/list-installations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/list-installations?${params}`, {
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
| `filterParam` | string | no | Optional installation filter field. Supported values are `mac` and `name`. |
| `filterValue` | string | no | Optional filter value used with Filter Parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "installations": [
        {}
      ],
      "pendingInstallations": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `installations` | array<object> | Installation summaries returned by the API. |
| `pendingInstallations` | number | Number of pending installation invitations. |
| `total` | number | Total number of matching installations. |

## Native endpoint

Through the native Airzone Cloud API, this operation is `GET /installations` (base URL `https://m.airzonecloud.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-installations.md) for the provider-specific parameters and requirements.

