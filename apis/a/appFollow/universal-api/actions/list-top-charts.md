# AppFollow: List Top Charts

Retrieves top chart results from AppFollow.

```
GET https://connect.mindcloud.co/v1/universal/appFollow/latest/actions/list-top-charts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AppFollow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appFollow/latest/actions/list-top-charts?connectionId=$CONNECTION_ID&country=string&device=string&genre=string&date=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "country": "string",
  "device": "string",
  "genre": "string",
  "date": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appFollow/latest/actions/list-top-charts?${params}`, {
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
| `country` | string | yes | Country code. |
| `device` | string | yes | Device type. |
| `genre` | string | yes | Genre code. |
| `date` | string | yes | Date. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AppFollow API returns.

## Native endpoint

Through the native AppFollow API, this operation is `GET /api/v2/charts/topcharts` (base URL `https://api.appfollow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-top-charts.md) for the provider-specific parameters and requirements.

