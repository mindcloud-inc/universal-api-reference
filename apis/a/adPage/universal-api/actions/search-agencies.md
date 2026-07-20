# AdPage: Search Agencies

Finds agencies in AdPage by name.

```
GET https://connect.mindcloud.co/v1/universal/adPage/latest/actions/search-agencies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AdPage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adPage/latest/actions/search-agencies?connectionId=$CONNECTION_ID&name=AdPage" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "AdPage"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adPage/latest/actions/search-agencies?${params}`, {
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
| `name` | string | yes | Agency name to search for. Example: `AdPage`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "colors": {
        "dark": "string",
        "fifth": "string",
        "fourth": "string",
        "primary": "string",
        "secondary": "string"
      },
      "domains": {
        "application": "string",
        "projects": "string"
      },
      "images": {
        "icon": "string",
        "logo": "string"
      },
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `colors.dark` | string |  |
| `colors.fifth` | string |  |
| `colors.fourth` | string |  |
| `colors.primary` | string |  |
| `colors.secondary` | string |  |
| `domains.application` | string |  |
| `domains.projects` | string |  |
| `images.icon` | string |  |
| `images.logo` | string |  |
| `name` | string |  |

## Native endpoint

Through the native AdPage API, this operation is `POST /api/agency/search` (base URL `https://whitelabel.adpage.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-agencies.md) for the provider-specific parameters and requirements.

