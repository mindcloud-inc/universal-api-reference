# Explorium: Enrich Prospect Social Media

Enriches prospects with social media in Explorium API.

```
GET https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/enrich-prospect-social-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Explorium `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/enrich-prospect-social-media?connectionId=$CONNECTION_ID&prospect_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "prospect_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/enrich-prospect-social-media?${params}`, {
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
| `prospect_id` | string | yes | The Explorium prospect identifier to enrich. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "responseContext": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `responseContext` | object | Raw API response context. |

## Native endpoint

Through the native Explorium API, this operation is `POST /v1/prospects/linkedin_posts/enrich` (base URL `https://api.explorium.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrich-prospect-social-media.md) for the provider-specific parameters and requirements.

