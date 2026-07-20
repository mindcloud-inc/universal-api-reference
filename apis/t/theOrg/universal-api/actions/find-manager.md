# The Org: Find Manager

Finds a manager in The Org by email or LinkedIn URL.

```
GET https://connect.mindcloud.co/v1/universal/theOrg/latest/actions/find-manager
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a The Org `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theOrg/latest/actions/find-manager?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/theOrg/latest/actions/find-manager?${params}`, {
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
| `email` | string | no | Email address of the person. |
| `linked_in_url` | string | no | LinkedIn profile URL of the person. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "manager": {},
        "position": {}
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.manager` | object | Resolved manager details |
| `data.position` | object | Matched position details |

## Native endpoint

Through the native The Org API, this operation is `GET /v1.1/companies/org-chart/managers` (base URL `https://api.theorg.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-manager.md) for the provider-specific parameters and requirements.

