# World News API: Retrieve Front Page

Retrieves a newspaper front page from World News API.

```
GET https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/retrieve-front-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a World News API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/retrieve-front-page?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/retrieve-front-page?${params}`, {
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
| `date` | date | no | Date of the newspaper front page to retrieve. |
| `sourceCountry` | string | no | Two-letter country code for the front page source. |
| `sourceName` | string | no | Provider source name for the newspaper front page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "front_page": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `front_page` | object | Front page metadata and image for the selected newspaper edition. |

## Native endpoint

Through the native World News API API, this operation is `GET /retrieve-front-page` (base URL `https://api.worldnewsapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-front-page.md) for the provider-specific parameters and requirements.

