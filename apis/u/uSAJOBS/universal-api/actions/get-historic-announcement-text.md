# USAJOBS: Get Historic Announcement Text

Retrieves historic announcement text from USAJOBS.

```
GET https://connect.mindcloud.co/v1/universal/uSAJOBS/latest/actions/get-historic-announcement-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a USAJOBS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uSAJOBS/latest/actions/get-historic-announcement-text?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uSAJOBS/latest/actions/get-historic-announcement-text?${params}`, {
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
| `hiringAgencyCodes` | string | no | Agency code in which the position is located. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native USAJOBS API returns.

## Native endpoint

Through the native USAJOBS API, this operation is `GET /api/historicjoa/announcementtext` (base URL `https://data.usajobs.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-historic-announcement-text.md) for the provider-specific parameters and requirements.

