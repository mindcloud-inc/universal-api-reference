# Geral: Get Splash Page

Retrieves a splash page from Geral by ID.

```
GET https://connect.mindcloud.co/v1/universal/geral/latest/actions/get-splash-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geral `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geral/latest/actions/get-splash-page?connectionId=$CONNECTION_ID&splashPageId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "splashPageId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geral/latest/actions/get-splash-page?${params}`, {
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
| `splashPageId` | number | yes | The splash page ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "datetime": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "last_datetime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string | Splash page color. |
| `datetime` | date | Creation timestamp. |
| `id` | number | Splash page ID. |
| `last_datetime` | date | Last update timestamp. |
| `name` | string | Splash page name. |

## Native endpoint

Through the native Geral API, this operation is `GET /splash-pages/:splash_page_id` (base URL `https://ger.al/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-splash-page.md) for the provider-specific parameters and requirements.

