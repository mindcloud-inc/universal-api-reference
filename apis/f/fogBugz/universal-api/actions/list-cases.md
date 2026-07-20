# FogBugz: List Cases

Retrieves cases from FogBugz.

```
GET https://connect.mindcloud.co/v1/universal/fogBugz/latest/actions/list-cases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FogBugz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fogBugz/latest/actions/list-cases?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fogBugz/latest/actions/list-cases?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sFilter` | string | no | Show only cases returned by a specific saved filter. |
| `max` | number | no | Maximum number of cases to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ixBug": 1,
      "operations": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ixBug` | number | Case ID. |
| `operations` | array<string> | Available case operations for the current user. |

## Native endpoint

Through the native FogBugz API, this operation is `POST /listCases` (base URL `{{credentials.siteUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-cases.md) for the provider-specific parameters and requirements.

