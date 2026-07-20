# Florm: Get Form Analytics

Retrieves analytics for a Florm form.

```
GET https://connect.mindcloud.co/v1/universal/florm/latest/actions/get-form-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Florm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/florm/latest/actions/get-form-analytics?connectionId=$CONNECTION_ID&formGuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formGuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/florm/latest/actions/get-form-analytics?${params}`, {
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
| `formGuid` | string | yes | GUID of the Florm form to analyze. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allSessions": 1,
      "finalSessions": 1,
      "guid": "string",
      "meta": {},
      "name": "Ava Chen",
      "sharedGuid": "string",
      "steps": [
        {}
      ],
      "urlParameters": [
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
| `allSessions` | number | Total session count when present. |
| `finalSessions` | number | Final session count when present. |
| `guid` | string | GUID of the analyzed form. |
| `meta` | object | Analytics metadata object. |
| `name` | string | Form name. |
| `sharedGuid` | string | Shared GUID of the analyzed form. |
| `steps` | array<object> | Per-step analytics. |
| `urlParameters` | array<object> | Analytics grouped by URL parameter. |

## Native endpoint

Through the native Florm API, this operation is `POST /v1/analytics/form/:form_guid` (base URL `https://api.florm.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-analytics.md) for the provider-specific parameters and requirements.

