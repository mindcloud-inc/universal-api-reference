# CINCEL: Download Team Signed Documents ZIP



```
GET https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/download-team-signed-documents-zip
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CINCEL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/download-team-signed-documents-zip?connectionId=$CONNECTION_ID&team=string&takeout=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "team": "string",
  "takeout": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/download-team-signed-documents-zip?${params}`, {
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
| `team` | string | yes | Team UUID from the path. |
| `takeout` | string | yes | Year or year-month period, for example `2026` or `2026-04`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Team takeout ZIP payload, exposed as a raw string by the current runtime mapping once signed documents exist for the requested period. |

## Native endpoint

Through the native CINCEL API, this operation is `GET /teams/:team/:takeout.zip` (base URL `https://api.cincel.digital/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-team-signed-documents-zip.md) for the provider-specific parameters and requirements.

