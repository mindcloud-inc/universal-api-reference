# Informizely: List Sites



```
GET https://connect.mindcloud.co/v1/universal/informizely/latest/actions/list-sites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Informizely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/informizely/latest/actions/list-sites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/informizely/latest/actions/list-sites?${params}`, {
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
| `includeSurveyData` | boolean | no | Set to false to exclude survey metadata from each site result. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Domain": "string",
      "Id": "string",
      "Surveys": [
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
| `Domain` | string | The site domain. |
| `Id` | string | The Informizely site ID. |
| `Surveys` | array<object> | The surveys attached to the site when includeSurveyData is true. |

## Native endpoint

Through the native Informizely API, this operation is `GET /sites` (base URL `https://api.informizely.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sites.md) for the provider-specific parameters and requirements.

